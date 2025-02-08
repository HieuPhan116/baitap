import Image from "next/image"
import Link from "next/link"
import { Card, CardContent } from "@/components/ui/card"

export default function Home() {
  return (
    <main className="min-h-screen bg-gradient-to-b from-pink-50 to-orange-50">
      {/* Hero Section - Reduced height by about 70% */}
      <div className="relative w-full h-[90px] md:h-[120px]">
        <Image
          src="https://hebbkx1anhila5yf.public.blob.vercel-storage.com/z6297110300115_5f19ffe551657b20de3dc0d636f3c89d.jpg-3CVC4Gtj8RU9TxcRMKc6ExklY3MoO8.jpeg"
          alt="Câu Lạc Bộ Bóng Đá Tỉnh Đồng Tháp Banner"
          fill
          priority
          className="object-cover object-center"
        />
        {/* Overlay to ensure text is readable */}
        <div className="absolute inset-0 bg-black bg-opacity-30 flex items-center justify-center">
          <h1 className="text-white text-2xl md:text-3xl font-bold text-center px-4">
            CÂU LẠC BỘ BÓNG ĐÁ TỈNH ĐỒNG THÁP
          </h1>
        </div>
      </div>

      {/* Content Section */}
      <div className="container mx-auto px-4 py-8 max-w-4xl">
        <Card className="border-none shadow-lg">
          <CardContent className="p-6 space-y-8">
            {/* Basic Information */}
            <section>
              <h2 className="text-2xl font-bold mb-4">Thông Tin Sơ Lược Về Câu Lạc Bộ</h2>
              <p className="text-lg pl-4">
                Tiền thân của đội là Đội bóng đá Đồng Tháp, thành lập năm 1976, do Sở Thể dục Thể thao Đồng Tháp quản lý
                và hiện tại cậu lạc bộ cũng có trang web chính thức{" "}
                <Link href="https://dongthapfc.org/" className="text-blue-600 hover:underline">
                  tại đây
                </Link>
                .
              </p>
            </section>

            {/* Logo Section */}
            <section className="text-center">
              <Image
                src="https://upload.wikimedia.org/wikipedia/vi/3/33/Dong_Thap_FC.png"
                alt="Logo chính thức Đồng Tháp FC"
                width={200}
                height={200}
                className="mx-auto"
              />
              <h3 className="text-xl font-semibold mt-4">Hình ảnh Logo chính thức</h3>
            </section>

            {/* Side Information */}
            <section>
              <h2 className="text-2xl font-bold mb-4">Thông Tin Bên Lề</h2>
              <p className="text-lg pl-4 mb-4">
                Từ lúc thành lập đến nay thì câu lạc bộ cũng có những giải thưởng to lớn có thể kể đến như đạt kết quả
                tốt ở mùa giải hạng Nhất năm 2014 và giành suất thăng hạng V.League.
              </p>
              <div className="relative w-full h-[300px] rounded-lg overflow-hidden">
                <Image
                  src="https://images2.thanhnien.vn/thumb_w/640/528068263637045248/2023/8/13/img-6313-1691935517068880061221.jpg"
                  alt="Đội bóng Đồng Tháp"
                  fill
                  className="object-cover"
                />
              </div>
            </section>

            {/* Registration Section */}
            <section>
              <h2 className="text-2xl font-bold mb-4">Đăng ký</h2>
              <p className="text-lg pl-4">
                Nếu bạn là người có đam mê, tài năng và muốn cống hiến với tư cách là đứa con của Đồng Tháp bạn có thể
                liên hệ chi tiết{" "}
                <Link href="https://dongthapfc.org/lien-he/" className="text-blue-600 hover:underline">
                  tại đây
                </Link>
              </p>
            </section>
          </CardContent>
        </Card>
      </div>
    </main>
  )
}


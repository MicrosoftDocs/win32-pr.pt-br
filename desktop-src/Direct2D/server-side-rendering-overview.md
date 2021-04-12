---
title: Usando Direct2D para renderização de Server-Side
description: Descreve o uso de Direct2D para renderização no lado do servidor.
ms.assetid: 12bf4f14-d86f-40ff-b3d3-15ffb3bd7300
keywords:
- Direct2D, renderização no lado do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35c9df619ee43d11c90c171598c87b6e447dd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366135"
---
# <a name="using-direct2d-for-server-side-rendering"></a><span data-ttu-id="1d6cd-104">Usando Direct2D para renderização de Server-Side</span><span class="sxs-lookup"><span data-stu-id="1d6cd-104">Using Direct2D for Server-Side Rendering</span></span>

<span data-ttu-id="1d6cd-105">O Direct2D é adequado para aplicativos gráficos que exigem renderização no lado do servidor no Windows Server.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-105">Direct2D is well-suited for graphics applications that require server-side rendering on Windows Server.</span></span> <span data-ttu-id="1d6cd-106">Esta visão geral descreve as noções básicas do uso do Direct2D para renderização no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-106">This overview describes the basics of using Direct2D for server-side rendering.</span></span> <span data-ttu-id="1d6cd-107">Ele contém as seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="1d6cd-107">It contains the following sections:</span></span>

-   [<span data-ttu-id="1d6cd-108">Requisitos para renderização de Server-Side</span><span class="sxs-lookup"><span data-stu-id="1d6cd-108">Requirements for Server-Side Rendering</span></span>](#requirements-for-server-side-rendering)
-   [<span data-ttu-id="1d6cd-109">Opções para APIs disponíveis</span><span class="sxs-lookup"><span data-stu-id="1d6cd-109">Options for Available APIs</span></span>](#options-for-available-apis)
    -   [<span data-ttu-id="1d6cd-110">GRÁFICA</span><span class="sxs-lookup"><span data-stu-id="1d6cd-110">GDI</span></span>](#gdi)
    -   [<span data-ttu-id="1d6cd-111">GDI+</span><span class="sxs-lookup"><span data-stu-id="1d6cd-111">GDI+</span></span>](#gdi)
    -   [<span data-ttu-id="1d6cd-112">Direct2D</span><span class="sxs-lookup"><span data-stu-id="1d6cd-112">Direct2D</span></span>](#using-direct2d-for-server-side-rendering)
-   [<span data-ttu-id="1d6cd-113">Como usar Direct2D para renderização de Server-Side</span><span class="sxs-lookup"><span data-stu-id="1d6cd-113">How to Use Direct2D for Server-Side Rendering</span></span>](#how-to-use-direct2d-for-server-side-rendering)
    -   [<span data-ttu-id="1d6cd-114">Renderização de software</span><span class="sxs-lookup"><span data-stu-id="1d6cd-114">Software Rendering</span></span>](#software-rendering)
    -   [<span data-ttu-id="1d6cd-115">Multithread</span><span class="sxs-lookup"><span data-stu-id="1d6cd-115">Multithreading</span></span>](#multithreading)
    -   [<span data-ttu-id="1d6cd-116">Gerando um arquivo de bitmap</span><span class="sxs-lookup"><span data-stu-id="1d6cd-116">Generating a Bitmap File</span></span>](#generating-a-bitmap-file)
-   [<span data-ttu-id="1d6cd-117">Conclusão</span><span class="sxs-lookup"><span data-stu-id="1d6cd-117">Conclusion</span></span>](#conclusion)
-   [<span data-ttu-id="1d6cd-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1d6cd-118">Related topics</span></span>](#related-topics)

## <a name="requirements-for-server-side-rendering"></a><span data-ttu-id="1d6cd-119">Requisitos para renderização de Server-Side</span><span class="sxs-lookup"><span data-stu-id="1d6cd-119">Requirements for Server-Side Rendering</span></span>

<span data-ttu-id="1d6cd-120">Este é um cenário típico para um servidor de gráfico: gráficos e gráficos são renderizados em um servidor e entregues como bitmaps em resposta a solicitações da Web.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-120">The following is a typical scenario for a chart server: charts and graphics are rendered on a server and delivered as bitmaps in response to Web requests.</span></span> <span data-ttu-id="1d6cd-121">O servidor pode estar equipado com uma placa gráfica de low-end ou sem placa gráfica.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-121">The server might be equipped with a low-end graphics card or no graphics card at all.</span></span>

<span data-ttu-id="1d6cd-122">Esse cenário revela três requisitos de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-122">This scenario reveals three application requirements.</span></span> <span data-ttu-id="1d6cd-123">Primeiro, o aplicativo deve lidar com várias solicitações simultâneas com eficiência, especialmente em servidores de vários núcleos.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-123">First, the application must handle multiple concurrent requests efficiently, especially on multicore servers.</span></span> <span data-ttu-id="1d6cd-124">Em segundo lugar, o aplicativo deve usar a renderização de software ao ser executado em servidores com uma placa gráfica de baixo nível ou sem placa gráfica.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-124">Second, the application must use software rendering when running on servers with a low-end graphics card or no graphics card.</span></span> <span data-ttu-id="1d6cd-125">Por fim, o aplicativo deve ser executado como um serviço na sessão 0 para que ele não exija que um usuário esteja conectado.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-125">Finally, the application must run as a service in Session 0 so that it does not require a user to be logged in.</span></span> <span data-ttu-id="1d6cd-126">Para obter mais informações sobre a sessão 0, consulte [impacto do isolamento da sessão 0 em serviços e drivers no Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).</span><span class="sxs-lookup"><span data-stu-id="1d6cd-126">For more information about Session 0, see [Impact of Session 0 Isolation on Services and Drivers in Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).</span></span>

## <a name="options-for-available-apis"></a><span data-ttu-id="1d6cd-127">Opções para APIs disponíveis</span><span class="sxs-lookup"><span data-stu-id="1d6cd-127">Options for Available APIs</span></span>

<span data-ttu-id="1d6cd-128">Há três opções para renderização no lado do servidor: GDI, GDI+ e Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-128">There are three options for server-side rendering: GDI, GDI+ and Direct2D.</span></span> <span data-ttu-id="1d6cd-129">Como o GDI e o GDI+, o Direct2D é uma API de renderização 2D nativa que fornece aos aplicativos mais controle sobre o uso de dispositivos gráficos.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-129">Like GDI and GDI+, Direct2D is a native 2D rendering API that gives applications more control over the use of graphics devices.</span></span> <span data-ttu-id="1d6cd-130">Além disso, o Direct2D dá suporte exclusivamente a uma fábrica de thread único e multithread.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-130">In addition, Direct2D uniquely supports a single-threaded and a multithreaded factory.</span></span> <span data-ttu-id="1d6cd-131">As seções a seguir comparam cada API em termos de qualidades de desenho e renderização multithread no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-131">The following sections compare each API in terms of drawing qualities and multithreaded server-side rendering.</span></span>

### <a name="gdi"></a><span data-ttu-id="1d6cd-132">GDI</span><span class="sxs-lookup"><span data-stu-id="1d6cd-132">GDI</span></span>

<span data-ttu-id="1d6cd-133">Ao contrário de Direct2D e GDI+, o GDI não oferece suporte a recursos de desenho de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-133">Unlike Direct2D and GDI+, GDI does not support high-quality drawing features.</span></span> <span data-ttu-id="1d6cd-134">Por exemplo, o GDI não dá suporte a anti-aliasing para a criação de linhas suaves e tem apenas suporte limitado para transparência.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-134">For instance, GDI does not support antialiasing for creating smooth lines and has only limited support for transparency.</span></span> <span data-ttu-id="1d6cd-135">Com base nos resultados do teste de desempenho de gráficos no Windows 7 e no Windows Server 2008 R2, o Direct2D escala com mais eficiência do que o GDI, apesar da reestruturação dos bloqueios no GDI.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-135">Based on the graphics performance test results on Windows 7 and Windows Server 2008 R2, Direct2D scales more efficiently than GDI, despite the redesign of locks in GDI.</span></span> <span data-ttu-id="1d6cd-136">Para obter mais informações sobre esses resultados de teste, consulte [engenharia de desempenho gráfico do Windows 7](/archive/blogs/e7/engineering-windows-7-graphics-performance).</span><span class="sxs-lookup"><span data-stu-id="1d6cd-136">For more information about these test results, see [Engineering Windows 7 Graphics Performance](/archive/blogs/e7/engineering-windows-7-graphics-performance).</span></span>

<span data-ttu-id="1d6cd-137">Além disso, os aplicativos que usam GDI são limitados a 10240 identificadores GDI por processo e 65536 identificadores GDI por sessão.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-137">In addition, applications using GDI are limited to 10240 GDI handles per process and 65536 GDI handles per session.</span></span> <span data-ttu-id="1d6cd-138">O motivo é que o Windows internamente usa uma palavra de 16 bits para armazenar o índice de identificadores de cada sessão.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-138">The reason is that internally Windows uses a 16-bit WORD to store the index of handles for each session.</span></span>

### <a name="gdi"></a><span data-ttu-id="1d6cd-139">GDI+</span><span class="sxs-lookup"><span data-stu-id="1d6cd-139">GDI+</span></span>

<span data-ttu-id="1d6cd-140">Embora o GDI+ dê suporte à interseção de suavização e alfa para desenho de alta qualidade, o principal problema com o GDI+ para cenários de servidor é que ele não dá suporte à execução na sessão 0.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-140">While GDI+ supports antialiasing and alpha blending for high-quality drawing, the main problem with GDI+ for server-scenarios is that it does not support running in Session 0.</span></span> <span data-ttu-id="1d6cd-141">Como a sessão 0 só dá suporte à funcionalidade não interativa, as funções que interagem direta ou indiretamente com dispositivos de exibição, portanto, receberão erros.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-141">Since Session 0 only supports non-interactive functionality, functions that directly or indirectly interact with display devices will therefore receive errors.</span></span> <span data-ttu-id="1d6cd-142">Exemplos específicos de funções incluem não apenas aqueles que lidam com dispositivos de vídeo, mas também aqueles que indiretamente lidam com drivers de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-142">Specific examples of functions include not only those dealing with display devices, but also those indirectly dealing with device drivers.</span></span>

<span data-ttu-id="1d6cd-143">Semelhante ao GDI, o GDI+ é limitado por seu mecanismo de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-143">Similar to GDI, GDI+ is limited by its locking mechanism.</span></span> <span data-ttu-id="1d6cd-144">Os mecanismos de bloqueio no GDI+ são os mesmos no Windows 7 e no Windows Server 2008 R2, como nas versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-144">The locking mechanisms in GDI+ are the same in Windows 7 and Windows Server 2008 R2 as in previous versions.</span></span>

### <a name="direct2d"></a><span data-ttu-id="1d6cd-145">Direct2D</span><span class="sxs-lookup"><span data-stu-id="1d6cd-145">Direct2D</span></span>

<span data-ttu-id="1d6cd-146">O Direct2D é uma API de gráficos 2D, de modo imediato e com aceleração de hardware que fornece alto desempenho e renderização de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-146">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high-quality rendering.</span></span> <span data-ttu-id="1d6cd-147">Ele oferece uma fábrica de thread único e multithread e o dimensionamento linear da renderização de software refinada do curso.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-147">It offers a single-threaded and a multithreaded factory and the linear scaling of course-grained software rendering.</span></span>

<span data-ttu-id="1d6cd-148">Para fazer isso, Direct2D define uma interface de fábrica raiz.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-148">To do this, Direct2D defines a root factory interface.</span></span> <span data-ttu-id="1d6cd-149">Como regra, um objeto criado em uma fábrica só pode ser usado com outros objetos criados na mesma fábrica.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-149">As a rule, an object created on a factory can only be used with other objects created from the same factory.</span></span> <span data-ttu-id="1d6cd-150">O chamador pode solicitar uma fábrica de thread único ou multithread quando ele é criado.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-150">The caller can request either a single-threaded or a multithreaded factory when it is created.</span></span> <span data-ttu-id="1d6cd-151">Se uma fábrica de thread único for solicitada, nenhum bloqueio de threads será executado.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-151">If a single-threaded factory is requested, then no locking of threads is performed.</span></span> <span data-ttu-id="1d6cd-152">Se o chamador solicitar uma fábrica multi-threaded, um bloqueio de thread em toda a fábrica será adquirido sempre que uma chamada for feita em Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-152">If the caller requests a multithreaded factory, then, a factory-wide thread lock is acquired whenever a call is made into Direct2D.</span></span>

<span data-ttu-id="1d6cd-153">Além disso, o bloqueio de threads em Direct2D é mais granular do que no GDI e no GDI+, para que o aumento do número de threads tenha um impacto mínimo sobre o desempenho.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-153">In addition, the locking of threads in Direct2D is more granular than in GDI and GDI+, so that the increase of the number of threads has minimal impact on the performance.</span></span>

## <a name="how-to-use-direct2d-for-server-side-rendering"></a><span data-ttu-id="1d6cd-154">Como usar Direct2D para renderização de Server-Side</span><span class="sxs-lookup"><span data-stu-id="1d6cd-154">How to Use Direct2D for Server-Side Rendering</span></span>

<span data-ttu-id="1d6cd-155">As seções a seguir descrevem como usar a renderização de software, como usar de forma ideal uma fábrica de thread único e multithread e como desenhar e salvar um desenho complexo em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-155">The following sections describe how to use software rendering, how to optimally use a single-threaded and a multithreaded factory, and how to draw and save a complex drawing to a file.</span></span>

### <a name="software-rendering"></a><span data-ttu-id="1d6cd-156">Renderização de software</span><span class="sxs-lookup"><span data-stu-id="1d6cd-156">Software Rendering</span></span>

<span data-ttu-id="1d6cd-157">Os aplicativos do lado do servidor usam a renderização de software criando o destino de renderização [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) , com o tipo de destino render definido como d2d1 de \_ tipo de destino de renderização \_ \_ \_ ou d2d1 \_ tipo de destino de renderização \_ \_ \_ padrão.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-157">Server-side applications use software rendering by creating [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target, with the render target type set to either D2D1\_RENDER\_TARGET\_TYPE\_SOFTWARE or D2D1\_RENDER\_TARGET\_TYPE\_DEFAULT.</span></span> <span data-ttu-id="1d6cd-158">Para obter mais informações sobre destinos de renderização [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) , consulte o método [**ID2D1Factory:: CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) ; para obter mais informações sobre os tipos de destino de renderização, consulte [**\_ tipo de \_ destino \_ de renderização d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).</span><span class="sxs-lookup"><span data-stu-id="1d6cd-158">For more information about [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render targets, see the [**ID2D1Factory::CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) method; for more information about the render target types, see [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).</span></span>

### <a name="multithreading"></a><span data-ttu-id="1d6cd-159">Multithreading</span><span class="sxs-lookup"><span data-stu-id="1d6cd-159">Multithreading</span></span>

<span data-ttu-id="1d6cd-160">Saber como criar e compartilhar fábricas e renderizar destinos entre threads pode afetar significativamente o desempenho de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-160">Knowing how to create and share factories and render targets across threads can significantly impact the performance of an application.</span></span> <span data-ttu-id="1d6cd-161">As três figuras a seguir mostram três abordagens variadas.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-161">The following three figures show three varied approaches.</span></span> <span data-ttu-id="1d6cd-162">A abordagem ideal é mostrada na Figura 3.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-162">The optimal approach is shown in figure 3.</span></span>

![diagrama multithread Direct2D com um único destino de renderização.](images/server-side-rendering-1.png)

<span data-ttu-id="1d6cd-164">Na Figura 1, diferentes threads compartilham a mesma fábrica e o mesmo destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-164">In figure 1, different threads share the same factory and the same render target.</span></span> <span data-ttu-id="1d6cd-165">Essa abordagem pode levar a resultados imprevisíveis em casos em que vários threads alteram simultaneamente o estado do destino de renderização compartilhado, como configurar simultaneamente a matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-165">This approach can lead to unpredictable results in cases when multiple threads simultaneously change the state of the shared render target, such as simultaneously setting the transformation matrix.</span></span> <span data-ttu-id="1d6cd-166">Como o bloqueio interno no Direct2D não sincroniza um recurso compartilhado, como destinos de renderização, essa abordagem pode fazer com que a chamada [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) falhe no thread 1, porque no thread 2, a chamada **BeginDraw** já está usando o destino de renderização compartilhado.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-166">As the internal locking in Direct2D does not synchronize a shared resource such as render targets, this approach can cause the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) call to fail in thread 1, because in thread 2, the **BeginDraw** call is already using the shared render target.</span></span>

![diagrama multithread Direct2D com vários destinos de renderização.](images/server-side-rendering-2.png)

<span data-ttu-id="1d6cd-168">Para evitar os resultados imprevisíveis encontrados na Figura 1, a Figura 2 mostra uma fábrica multi-threaded com cada thread com seu próprio destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-168">To avoid the unpredictable results encountered in figure 1, figure 2 shows a multithreaded factory with each thread having its own render target.</span></span> <span data-ttu-id="1d6cd-169">Essa abordagem funciona, mas efetivamente funciona como um aplicativo de thread único.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-169">This approach works but it effectively functions as a single-threaded application.</span></span> <span data-ttu-id="1d6cd-170">O motivo é que o bloqueio de toda a fábrica se aplica somente ao nível de operação de desenho e todas as chamadas de desenho na mesma fábrica, consequentemente, são serializadas.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-170">The reason is that the factory-wide lock applies only to the drawing-operation level and all the drawing calls in the same factory consequently are serialized.</span></span> <span data-ttu-id="1d6cd-171">Como resultado, o thread 1 torna-se bloqueado durante a tentativa de inserir uma chamada de desenho, enquanto o thread 2 está no meio da execução de outra chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-171">As a result, thread 1 becomes blocked when trying to enter a drawing call, while thread 2 is in the middle of executing another drawing call.</span></span>

![diagrama multithread Direct2D com várias fábricas e vários destinos de renderização.](images/server-side-rendering-3.png)

<span data-ttu-id="1d6cd-173">A Figura 3 mostra a abordagem ideal, em que uma fábrica de thread único e um destino de renderização de thread único são usados.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-173">Figure 3 shows the optimal approach, where a single-threaded factory and a single-threaded render target are used.</span></span> <span data-ttu-id="1d6cd-174">Como nenhum bloqueio é executado ao usar uma fábrica de thread único, as operações de desenho em cada thread podem ser executadas simultaneamente para alcançar o desempenho ideal.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-174">Since no locking is performed when using a single-threaded factory, drawing operations in each thread can run concurrently to achieve optimal performance.</span></span>

### <a name="generating-a-bitmap-file"></a><span data-ttu-id="1d6cd-175">Gerando um arquivo de bitmap</span><span class="sxs-lookup"><span data-stu-id="1d6cd-175">Generating a Bitmap File</span></span>

<span data-ttu-id="1d6cd-176">Para gerar um arquivo de bitmap usando a renderização de software, use um destino de renderização [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="1d6cd-176">To generate a bitmap file using software rendering, use an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target.</span></span> <span data-ttu-id="1d6cd-177">Use um [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) para gravar o bitmap em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-177">Use an [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) to write the bitmap to a file.</span></span> <span data-ttu-id="1d6cd-178">Use [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) para codificar o bitmap em um formato de imagem especificado.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-178">Use [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) to encode the bitmap into a specified image format.</span></span> <span data-ttu-id="1d6cd-179">O exemplo de código a seguir mostra como desenhar e salvar a imagem a seguir em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-179">The following code example shows how to draw and save the following image to a file.</span></span>

![exemplo de imagem de saída.](images/saveasimagefile-sample.png)

<span data-ttu-id="1d6cd-181">Este exemplo de código cria primeiro um [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) e um destino de renderização [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="1d6cd-181">This code example first creates an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) and an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target.</span></span> <span data-ttu-id="1d6cd-182">Em seguida, ele renderiza um desenho com algum texto, uma geometria de caminho que representa um vidro de hora e uma hora transformada em um bitmap de WIC.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-182">It then renders a drawing with some text, a path geometry representing an hour glass, and a transformed hour glass into a WIC bitmap.</span></span> <span data-ttu-id="1d6cd-183">Em seguida, ele usa [IWICStream:: InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) para salvar o bitmap em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-183">It then uses [IWICStream::InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) to save the bitmap to a file.</span></span> <span data-ttu-id="1d6cd-184">Se seu aplicativo precisar salvar o bitmap na memória, use [IWICStream:: InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-184">If your application needs to save the bitmap in memory, use [IWICStream::InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) instead.</span></span> <span data-ttu-id="1d6cd-185">Por fim, ele usa [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) para codificar o bitmap.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-185">Finally, it uses [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) to encode the bitmap.</span></span>


```C++
// Create an IWICBitmap and RT
static const UINT sc_bitmapWidth = 640;
static const UINT sc_bitmapHeight = 480;
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateBitmap(
        sc_bitmapWidth,
        sc_bitmapHeight,
        GUID_WICPixelFormat32bppBGR,
        WICBitmapCacheOnLoad,
        &pWICBitmap
        );
}

// Set the render target type to D2D1_RENDER_TARGET_TYPE_DEFAULT to use software rendering.
if (SUCCEEDED(hr))
{
    hr = pD2DFactory->CreateWicBitmapRenderTarget(
        pWICBitmap,
        D2D1::RenderTargetProperties(),
        &pRT
        );
}

// Create text format and a path geometry representing an hour glass. 
if (SUCCEEDED(hr))
{
    static const WCHAR sc_fontName[] = L"Calibri";
    static const FLOAT sc_fontSize = 50;

    hr = pDWriteFactory->CreateTextFormat(
        sc_fontName,
        NULL,
        DWRITE_FONT_WEIGHT_NORMAL,
        DWRITE_FONT_STYLE_NORMAL,
        DWRITE_FONT_STRETCH_NORMAL,
        sc_fontSize,
        L"", //locale
        &pTextFormat
        );
}
if (SUCCEEDED(hr))
{
    pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    hr = pD2DFactory->CreatePathGeometry(&pPathGeometry);
}
if (SUCCEEDED(hr))
{
    hr = pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_ALTERNATE);

    pSink->BeginFigure(
        D2D1::Point2F(0, 0),
        D2D1_FIGURE_BEGIN_FILLED
        );

    pSink->AddLine(D2D1::Point2F(200, 0));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(150, 50),
            D2D1::Point2F(150, 150),
            D2D1::Point2F(200, 200))
        );

    pSink->AddLine(D2D1::Point2F(0, 200));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(50, 150),
            D2D1::Point2F(50, 50),
            D2D1::Point2F(0, 0))
        );

    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}
if (SUCCEEDED(hr))
{
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 1.f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = pRT->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(100, 0),
            D2D1::Point2F(100, 200)),
        D2D1::BrushProperties(),
        pGradientStops,
        &pLGBrush
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        );
}
if (SUCCEEDED(hr))
{
    // Render into the bitmap.
    pRT->BeginDraw();
    pRT->Clear(D2D1::ColorF(D2D1::ColorF::White));
    D2D1_SIZE_F rtSize = pRT->GetSize();

    // Set the world transform to a 45 degree rotation at the center of the render target
    // and write "Hello, World".
    pRT->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45,
            D2D1::Point2F(
                rtSize.width / 2,
                rtSize.height / 2))
            );

    static const WCHAR sc_helloWorld[] = L"Hello, World!";
    pRT->DrawText(
        sc_helloWorld,
        ARRAYSIZE(sc_helloWorld) - 1,
        pTextFormat,
        D2D1::RectF(0, 0, rtSize.width, rtSize.height),
        pBlackBrush);

    // Reset back to the identity transform.
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(0, rtSize.height - 200));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(rtSize.width - 200, 0));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    hr = pRT->EndDraw();
}

if (SUCCEEDED(hr))
{
    // Save the image to a file.
    hr = pWICFactory->CreateStream(&pStream);
}

WICPixelFormatGUID format = GUID_WICPixelFormatDontCare;

// Use InitializeFromFilename to write to a file. If there is need to write inside the memory, use InitializeFromMemory. 
if (SUCCEEDED(hr))
{
    static const WCHAR filename[] = L"output.png";
    hr = pStream->InitializeFromFilename(filename, GENERIC_WRITE);
}
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateEncoder(GUID_ContainerFormatPng, NULL, &pEncoder);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Initialize(pStream, WICBitmapEncoderNoCache);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->CreateNewFrame(&pFrameEncode, NULL);
}
// Use IWICBitmapFrameEncode to encode the bitmap into the picture format you want.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Initialize(NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetSize(sc_bitmapWidth, sc_bitmapHeight);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetPixelFormat(&format);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->WriteSource(pWICBitmap, NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Commit();
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Commit();
}

```



## <a name="conclusion"></a><span data-ttu-id="1d6cd-186">Conclusão</span><span class="sxs-lookup"><span data-stu-id="1d6cd-186">Conclusion</span></span>

<span data-ttu-id="1d6cd-187">Como visto no acima, usar Direct2D para renderização no lado do servidor é simples e direto.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-187">As seen from the above, using Direct2D for server-side rendering is simple and straightforward.</span></span> <span data-ttu-id="1d6cd-188">Além disso, ele fornece alta qualidade e renderização altamente paralelizáveis que podem ser executadas em ambientes de baixo privilégio do servidor.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-188">In addition, it provides high quality and highly parallelizable rendering that can run in low-privilege environments of the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d6cd-189">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1d6cd-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d6cd-190">Referência de Direct2D</span><span class="sxs-lookup"><span data-stu-id="1d6cd-190">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 
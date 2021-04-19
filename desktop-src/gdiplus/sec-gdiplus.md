---
description: Este tópico fornece informações sobre considerações de segurança relacionadas à programação com o Windows GDI+.
ms.assetid: 411e16e4-ad8f-4567-8964-564f08283ba5
title: 'Considerações de segurança: GDI+'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d8c9d50393708e58651566ee90adcb4339cb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988854"
---
# <a name="security-considerations-gdi"></a><span data-ttu-id="addfd-103">Considerações de segurança: GDI+</span><span class="sxs-lookup"><span data-stu-id="addfd-103">Security Considerations: GDI+</span></span>

<span data-ttu-id="addfd-104">Este tópico fornece informações sobre considerações de segurança relacionadas à programação com o Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="addfd-104">This topic provides information about security considerations related to programming with Windows GDI+.</span></span> <span data-ttu-id="addfd-105">Este tópico não fornece tudo o que você precisa saber sobre problemas de segurança — em vez disso, use-o como ponto de partida e referência para essa área de tecnologia.</span><span class="sxs-lookup"><span data-stu-id="addfd-105">This topic doesn't provide all you need to know about security issues—instead, use it as a starting point and reference for this technology area.</span></span>

-   [<span data-ttu-id="addfd-106">Verificando o êxito dos construtores</span><span class="sxs-lookup"><span data-stu-id="addfd-106">Verifying the Success of Constructors</span></span>](#verifying-the-success-of-constructors)
-   [<span data-ttu-id="addfd-107">Alocando buffers</span><span class="sxs-lookup"><span data-stu-id="addfd-107">Allocating Buffers</span></span>](#allocating-buffers)
-   [<span data-ttu-id="addfd-108">Verificação de erros</span><span class="sxs-lookup"><span data-stu-id="addfd-108">Error Checking</span></span>](#error-checking)
-   [<span data-ttu-id="addfd-109">Sincronização de Thread </span><span class="sxs-lookup"><span data-stu-id="addfd-109">Thread Synchronization</span></span>](#thread-synchronization)
-   [<span data-ttu-id="addfd-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="addfd-110">Related topics</span></span>](#related-topics)

## <a name="verifying-the-success-of-constructors"></a><span data-ttu-id="addfd-111">Verificando o êxito dos construtores</span><span class="sxs-lookup"><span data-stu-id="addfd-111">Verifying the Success of Constructors</span></span>

<span data-ttu-id="addfd-112">Muitas das classes GDI+ fornecem um método [**Image:: GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) que você pode chamar para determinar se os métodos invocados em um objeto são bem-sucedidos.</span><span class="sxs-lookup"><span data-stu-id="addfd-112">Many of the GDI+ classes provide a [**Image::GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) method that you can call to determine whether methods invoked on an object are successful.</span></span> <span data-ttu-id="addfd-113">Você também pode chamar **Image:: GetLastStatus** para determinar se um construtor é bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="addfd-113">You can also call **Image::GetLastStatus** to determine whether a constructor is successful.</span></span>

<span data-ttu-id="addfd-114">O exemplo a seguir mostra como construir um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e chamar o método [**Image:: GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) para determinar se o Construtor foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="addfd-114">The following example shows how to construct an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and call the [**Image::GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) method to determine whether the constructor was successful.</span></span> <span data-ttu-id="addfd-115">Os valores **OK** e **InvalidParameter** são elementos da enumeração de [**status**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) .</span><span class="sxs-lookup"><span data-stu-id="addfd-115">The values **Ok** and **InvalidParameter** are elements of the [**Status**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) enumeration.</span></span>


```C++
Image myImage(L"Climber.jpg");
Status st = myImage.GetLastStatus();

if(Ok == st)
   // The constructor was successful. Use myImage.
else if(InvalidParameter == st)
   // The constructor failed because of an invalid parameter.
else
   // Compare st to other elements of the Status 
   // enumeration or do general error processing.
```



## <a name="allocating-buffers"></a><span data-ttu-id="addfd-116">Alocando buffers</span><span class="sxs-lookup"><span data-stu-id="addfd-116">Allocating Buffers</span></span>

<span data-ttu-id="addfd-117">Vários métodos GDI+ retornam dados numéricos ou de caractere em um buffer que é alocado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="addfd-117">Several GDI+ methods return numeric or character data in a buffer that is allocated by the caller.</span></span> <span data-ttu-id="addfd-118">Para cada um desses métodos, há um método complementar que fornece o tamanho do buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="addfd-118">For each of those methods, there is a companion method that gives the size of the required buffer.</span></span> <span data-ttu-id="addfd-119">Por exemplo, o método [**GraphicsPath:: GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) retorna uma matriz de objetos [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="addfd-119">For example, the [**GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) method returns an array of [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span> <span data-ttu-id="addfd-120">Antes de chamar **GraphicsPath:: GetPathPoints**, você deve alocar um buffer grande o suficiente para manter essa matriz.</span><span class="sxs-lookup"><span data-stu-id="addfd-120">Before you call **GraphicsPath::GetPathPoints**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="addfd-121">Você pode determinar o tamanho do buffer necessário chamando o método [**GraphicsPath:: GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) de um objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="addfd-121">You can determine the size of the required buffer by calling the [**GraphicsPath::GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) method of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span>

<span data-ttu-id="addfd-122">O exemplo a seguir mostra como determinar o número de pontos em um objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) , alocar um buffer grande o suficiente para conter vários pontos e, em seguida, chamar [**GraphicsPath:: GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) para preencher o buffer.</span><span class="sxs-lookup"><span data-stu-id="addfd-122">The following example shows how to determine the number of points in a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object, allocate a buffer large enough to hold that many points, and then call [**GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) to fill the buffer.</span></span> <span data-ttu-id="addfd-123">Antes que o código chame **GraphicsPath:: GetPathPoints**, ele verifica se a alocação do buffer foi bem-sucedida, certificando-se de que o ponteiro do buffer não seja **nulo**.</span><span class="sxs-lookup"><span data-stu-id="addfd-123">Before the code calls **GraphicsPath::GetPathPoints**, it verifies that the buffer allocation was successful by making sure that the buffer pointer is not **NULL**.</span></span>


```C++
GraphicsPath path;
path.AddEllipse(10, 10, 200, 100);

INT count = path.GetPointCount();          // get the size
Point* pointArray = new Point[count];      // allocate the buffer

if(pointArray)  // Check for successful allocation.
{
   path.GetPathPoints(pointArray, count);  // get the data
   ...                                     // use pointArray
   delete[] pointArray;                    // release the buffer
   pointArray = NULL;
}
```



<span data-ttu-id="addfd-124">O exemplo anterior usa o novo operador para alocar um buffer.</span><span class="sxs-lookup"><span data-stu-id="addfd-124">The previous example uses the new operator to allocate a buffer.</span></span> <span data-ttu-id="addfd-125">O novo operador era conveniente porque o buffer foi preenchido com um número conhecido de objetos [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="addfd-125">The new operator was convenient because the buffer was filled with a known number of [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span> <span data-ttu-id="addfd-126">Em alguns casos, o GDI+ grava mais em buffer do que uma matriz de objetos GDI+.</span><span class="sxs-lookup"><span data-stu-id="addfd-126">In some cases, GDI+ writes more into buffer than an array of GDI+ objects.</span></span> <span data-ttu-id="addfd-127">Às vezes, um buffer é preenchido com uma matriz de objetos GDI+, juntamente com dados adicionais que são apontados por membros desses objetos.</span><span class="sxs-lookup"><span data-stu-id="addfd-127">Sometimes a buffer is filled with an array of GDI+ objects along with additional data that is pointed to by members of those objects.</span></span> <span data-ttu-id="addfd-128">Por exemplo, o método [**Image:: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) retorna uma matriz de objetos [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) , um para cada item de propriedade (parte dos metadados) armazenado na imagem.</span><span class="sxs-lookup"><span data-stu-id="addfd-128">For example, the [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) method returns an array of [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) objects, one for each property item (piece of metadata) stored in the image.</span></span> <span data-ttu-id="addfd-129">Mas **Image:: GetAllPropertyItems** retorna mais do que apenas a matriz de objetos **PropertyItem** ; Ele acrescenta a matriz com dados adicionais.</span><span class="sxs-lookup"><span data-stu-id="addfd-129">But **Image::GetAllPropertyItems** returns more than just the array of **PropertyItem** objects; it appends the array with additional data.</span></span>

<span data-ttu-id="addfd-130">Antes de chamar [**Image:: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems), você deve alocar um buffer grande o suficiente para manter a matriz de objetos [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) junto com os dados adicionais.</span><span class="sxs-lookup"><span data-stu-id="addfd-130">Before you call [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems), you must allocate a buffer large enough to hold the array of [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) objects along with the additional data.</span></span> <span data-ttu-id="addfd-131">Você pode chamar o método [**Image:: GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) de um objeto Image para determinar o tamanho total do buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="addfd-131">You can call the [**Image::GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) method of an Image object to determine the total size of the required buffer.</span></span>

<span data-ttu-id="addfd-132">O exemplo a seguir mostra como criar um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e, posteriormente, chamar o método [**Image:: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) desse objeto **Image** para recuperar todos os itens de propriedade (metadados) armazenados na imagem.</span><span class="sxs-lookup"><span data-stu-id="addfd-132">The following example shows how to create an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and later call the [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) method of that **Image** object to retrieve all the property items (metadata) stored in the image.</span></span> <span data-ttu-id="addfd-133">O código aloca um buffer com base em um valor de tamanho retornado pelo método [**Image:: GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) .</span><span class="sxs-lookup"><span data-stu-id="addfd-133">The code allocates a buffer based on a size value returned by the [**Image::GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) method.</span></span> <span data-ttu-id="addfd-134">**Image:: GetPropertySize** também retorna um valor Count que fornece o número de itens de propriedade na imagem.</span><span class="sxs-lookup"><span data-stu-id="addfd-134">**Image::GetPropertySize** also returns a count value that gives the number of property items in the image.</span></span> <span data-ttu-id="addfd-135">Observe que o código não calcula o tamanho do buffer como `count*sizeof(PropertyItem)` .</span><span class="sxs-lookup"><span data-stu-id="addfd-135">Notice that the code does not calculate the buffer size as `count*sizeof(PropertyItem)`.</span></span> <span data-ttu-id="addfd-136">Um buffer calculado dessa maneira seria muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="addfd-136">A buffer calculated that way would be too small.</span></span>


```C++
UINT count = 0;
UINT size = 0;
Image myImage(L"FakePhoto.jpg");
myImage.GetPropertySize(&size, &count);

// GetAllPropertyItems returns an array of PropertyItem objects
// along with additional data. Allocate a buffer large enough to 
// receive the array and the additional data.
PropertyItem* propBuffer =(PropertyItem*)malloc(size);

if(propBuffer)
{
   myImage.GetAllPropertyItems(size, count, propBuffer);
   ...
   free(propBuffer);
   propBuffer = NULL;
}
```



## <a name="error-checking"></a><span data-ttu-id="addfd-137">Verificação de erros</span><span class="sxs-lookup"><span data-stu-id="addfd-137">Error Checking</span></span>

<span data-ttu-id="addfd-138">A maioria dos exemplos de código na documentação do GDI+ não mostra a verificação de erros.</span><span class="sxs-lookup"><span data-stu-id="addfd-138">Most of the code examples in the GDI+ documentation do not show error checking.</span></span> <span data-ttu-id="addfd-139">A verificação de erros completa torna um exemplo de código muito maior e pode obscurecer o ponto que está sendo ilustrado pelo exemplo.</span><span class="sxs-lookup"><span data-stu-id="addfd-139">Complete error checking makes a code example much longer and can obscure the point being illustrated by the example.</span></span> <span data-ttu-id="addfd-140">Você não deve colar exemplos da documentação diretamente no código de produção; em vez disso, você deve aprimorar os exemplos adicionando sua própria verificação de erro.</span><span class="sxs-lookup"><span data-stu-id="addfd-140">You should not paste examples from the documentation directly into production code; rather, you should enhance the examples by adding your own error checking.</span></span>

<span data-ttu-id="addfd-141">O exemplo a seguir mostra uma maneira de implementar a verificação de erros com o GDI+.</span><span class="sxs-lookup"><span data-stu-id="addfd-141">The following example shows one way of implementing error checking with GDI+.</span></span> <span data-ttu-id="addfd-142">Cada vez que um objeto GDI+ é construído, o código verifica se o Construtor foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="addfd-142">Each time a GDI+ object is constructed, the code checks to see whether the constructor was successful.</span></span> <span data-ttu-id="addfd-143">Essa verificação é especialmente importante para o construtor [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , que depende da leitura de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="addfd-143">That check is especially important for the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) constructor, which relies on reading a file.</span></span> <span data-ttu-id="addfd-144">Se todos os quatro objetos GDI+ ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image** e [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) forem construídos com êxito, o código chamará os métodos nesses objetos.</span><span class="sxs-lookup"><span data-stu-id="addfd-144">If all four of the GDI+ objects ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image**, and [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) are constructed successfully, the code calls methods on those objects.</span></span> <span data-ttu-id="addfd-145">Cada chamada de método é verificada quanto ao sucesso e, em caso de falha, as chamadas de método restantes são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="addfd-145">Each method call is checked for success, and in the event of failure, the remaining method calls are skipped.</span></span>


```C++
Status GdipExample(HDC hdc)
{
   Status status = GenericError;
   INT count = 0;
   Point* points = NULL;

   Graphics graphics(hdc);
   status = graphics.GetLastStatus();
   if(Ok != status)
      return status;

   GraphicsPath path;
   status = path.GetLastStatus();
   if(Ok != status)
      return status;

   Image image(L"MyTexture.bmp");
   status = image.GetLastStatus();
   if(Ok != status)
      return status;

   TextureBrush brush(&image);
   status = brush.GetLastStatus();
   if(Ok != status)
      return status;

   status = path.AddEllipse(10, 10, 200, 100);

   if(Ok == status)
   {
      status = path.AddBezier(40, 130, 200, 130, 200, 200, 60, 200);
   }
  
   if(Ok == status)
   {
      count = path.GetPointCount();
      status = path.GetLastStatus();
   }

   if(Ok == status)
   {
      points = new Point[count];

      if(NULL == points)
         status = OutOfMemory;
   }

   if(Ok == status)
   {
      status = path.GetPathPoints(points, count);  
   }
  
   if(Ok == status)
   {
      status = graphics.FillPath(&brush, &path);
   }
   
   if(Ok == status)
   {
      for(int j = 0; j < count; ++j)
      {
         status = graphics.FillEllipse(
         &brush, points[j].X - 5, points[j].Y - 5, 10, 10);
      }
   }

   if(points)
   {
      delete[] points;
      points = NULL;
   }

   return status;
}
```



## <a name="thread-synchronization"></a><span data-ttu-id="addfd-146">Sincronização de thread</span><span class="sxs-lookup"><span data-stu-id="addfd-146">Thread Synchronization</span></span>

<span data-ttu-id="addfd-147">É possível que mais de um thread tenha acesso a um único objeto GDI+.</span><span class="sxs-lookup"><span data-stu-id="addfd-147">It is possible for more than one thread to have access to a single GDI+ object.</span></span> <span data-ttu-id="addfd-148">No entanto, o GDI+ não fornece nenhum mecanismo de sincronização automático.</span><span class="sxs-lookup"><span data-stu-id="addfd-148">However, GDI+ does not provide any automatic synchronization mechanism.</span></span> <span data-ttu-id="addfd-149">Portanto, se dois threads em seu aplicativo tiverem um ponteiro para o mesmo objeto GDI+, será sua responsabilidade sincronizar o acesso a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="addfd-149">So if two threads in your application have a pointer to the same GDI+ object, it is your responsibility to synchronize access to that object.</span></span>

<span data-ttu-id="addfd-150">Alguns métodos de GDI+ retornam o **loadbusy** se um thread tenta chamar um método enquanto outro thread está executando um método no mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="addfd-150">Some GDI+ methods return **ObjectBusy** if a thread attempts to call a method while another thread is executing a method on the same object.</span></span> <span data-ttu-id="addfd-151">Não tente sincronizar o acesso a um objeto com base no valor de retorno de **loadbusy** .</span><span class="sxs-lookup"><span data-stu-id="addfd-151">Do not try to synchronize access to an object based on the **ObjectBusy** return value.</span></span> <span data-ttu-id="addfd-152">Em vez disso, sempre que você acessar um membro ou chamar um método do objeto, coloque a chamada dentro de uma seção crítica ou use alguma outra técnica de sincronização padrão.</span><span class="sxs-lookup"><span data-stu-id="addfd-152">Instead, each time you access a member or call a method of the object, place the call inside a critical section, or use some other standard synchronization technique.</span></span>

## <a name="related-topics"></a><span data-ttu-id="addfd-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="addfd-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="addfd-154">MSDN Security Developer Center</span><span class="sxs-lookup"><span data-stu-id="addfd-154">MSDN Security Developer Center</span></span>](https://msdn.microsoft.com/security/)
</dt> <dt>

<span data-ttu-id="addfd-155">[Recursos de How-To de segurança](/previous-versions/msp-n-p/ff650055(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="addfd-155">[Security How-To Resources](/previous-versions/msp-n-p/ff650055(v=pandp.10))</span></span>
</dt> <dt>

[<span data-ttu-id="addfd-156">Central de segurança do TechNet</span><span class="sxs-lookup"><span data-stu-id="addfd-156">TechNet Security Center</span></span>](https://technet.microsoft.com/security/)
</dt> </dl>

 

 

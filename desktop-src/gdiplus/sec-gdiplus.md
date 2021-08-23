---
description: Este tópico fornece informações sobre considerações de segurança relacionadas à programação com Windows GDI+.
ms.assetid: 411e16e4-ad8f-4567-8964-564f08283ba5
title: 'Considerações sobre segurança: GDI+'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc741911af403f079d16b4759431eaaa4b6cf55d5dad11826768033036aef75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035994"
---
# <a name="security-considerations-gdi"></a>Considerações sobre segurança: GDI+

Este tópico fornece informações sobre considerações de segurança relacionadas à programação com Windows GDI+. Este tópico não fornece tudo o que você precisa saber sobre problemas de segurança– em vez disso, use-o como um ponto de partida e uma referência para essa área de tecnologia.

-   [Verificando o sucesso dos construtores](#verifying-the-success-of-constructors)
-   [Alocando buffers](#allocating-buffers)
-   [Verificação de erro](#error-checking)
-   [Sincronização de Thread ](#thread-synchronization)
-   [Tópicos relacionados](#related-topics)

## <a name="verifying-the-success-of-constructors"></a>Verificando o sucesso dos construtores

Muitas das classes GDI+ fornecem um método [**Image::GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) que você pode chamar para determinar se os métodos invocados em um objeto são bem-sucedidos. Você também pode chamar **Image::GetLastStatus** para determinar se um construtor foi bem-sucedido.

O exemplo a seguir mostra como construir um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e chamar o método [**Image::GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) para determinar se o construtor foi bem-sucedido. Os valores **OK** e **InvalidParameter** são elementos da [**enumeração Status.**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status)


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



## <a name="allocating-buffers"></a>Alocando buffers

Vários GDI+ retornam dados numéricos ou de caracteres em um buffer alocado pelo chamador. Para cada um desses métodos, há um método de adendo que fornece o tamanho do buffer necessário. Por exemplo, o [**método GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) retorna uma matriz de [**objetos**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) Point. Antes de chamar **GraphicsPath::GetPathPoints,** você deve alocar um buffer grande o suficiente para manter essa matriz. Você pode determinar o tamanho do buffer necessário chamando o [**método GraphicsPath::GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) de um [**objeto GraphicsPath.**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath)

O exemplo a seguir mostra como determinar o número de pontos em um objeto [**GraphicsPath,**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) alocar um buffer grande o suficiente para manter tantos pontos e, em seguida, chamar [**GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) para preencher o buffer. Antes que o código chama **GraphicsPath::GetPathPoints**, ele verifica se a alocação de buffer foi bem-sucedida, certificando-se de que o ponteiro do buffer não seja **NULL.**


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



O exemplo anterior usa o novo operador para alocar um buffer. O novo operador foi conveniente porque o buffer foi preenchido com um número conhecido de [**objetos Point.**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) Em alguns casos, GDI+ mais no buffer do que uma matriz de GDI+ objetos. Às vezes, um buffer é preenchido com uma matriz de objetos GDI+ juntamente com dados adicionais que são apontados por membros desses objetos. Por exemplo, o método [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) retorna uma matriz de objetos [**PropertyItem,**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) um para cada item de propriedade (parte dos metadados) armazenado na imagem. Mas **Image::GetAllPropertyItems** retorna mais do que apenas a matriz de **objetos PropertyItem;** ele anexa a matriz com dados adicionais.

Antes de chamar [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems), você deve alocar um buffer grande o suficiente para manter a matriz de objetos [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) junto com os dados adicionais. Você pode chamar o [**método Image::GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) de um objeto Image para determinar o tamanho total do buffer necessário.

O exemplo [**a**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) seguir mostra como criar um objeto Image e, posteriormente, chamar o método [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) desse objeto **Image** para recuperar todos os itens de propriedade (metadados) armazenados na imagem. O código aloca um buffer com base em um valor de tamanho retornado pelo método [**Image::GetPropertySize.**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) **Image::GetPropertySize** também retorna um valor de contagem que fornece o número de itens de propriedade na imagem. Observe que o código não calcula o tamanho do buffer como `count*sizeof(PropertyItem)` . Um buffer calculado dessa forma seria muito pequeno.


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



## <a name="error-checking"></a>Verificação de erro

A maioria dos exemplos de código na documentação GDI+ não mostra a verificação de erro. A verificação de erros completa torna um exemplo de código muito mais longo e pode obscurecer o ponto que está sendo ilustrado pelo exemplo. Você não deve colar exemplos da documentação diretamente no código de produção; Em vez disso, você deve aprimorar os exemplos adicionando sua própria verificação de erro.

O exemplo a seguir mostra uma maneira de implementar a verificação de erros com GDI+. Sempre que um GDI+ objeto é construído, o código verifica se o construtor foi bem-sucedido. Essa verificação é especialmente importante para o [**construtor image,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) que depende da leitura de um arquivo. Se todos os quatro objetos GDI+ ([**Graphics,**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) [**GraphicsPath,**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) **Image** e [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) são construídos com êxito, o código chama métodos nesses objetos. Cada chamada de método é verificada quanto ao sucesso e, em caso de falha, as chamadas de método restantes são ignoradas.


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



## <a name="thread-synchronization"></a>Sincronização de thread

É possível que mais de um thread tenha acesso a um único GDI+ objeto. No entanto, GDI+ não fornece nenhum mecanismo de sincronização automática. Portanto, se dois threads em seu aplicativo têm um ponteiro para o mesmo objeto GDI+, é sua responsabilidade sincronizar o acesso a esse objeto.

Alguns GDI+ retornarão **ObjectBusy** se um thread tentar chamar um método enquanto outro thread estiver executando um método no mesmo objeto. Não tente sincronizar o acesso a um objeto com base no valor de **retorno ObjectBusy.** Em vez disso, sempre que você acessar um membro ou chamar um método do objeto , coloque a chamada dentro de uma seção crítica ou use alguma outra técnica de sincronização padrão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[MSDN Security Developer Center](https://msdn.microsoft.com/security/)
</dt> <dt>

[Recursos de How-To segurança](/previous-versions/msp-n-p/ff650055(v=pandp.10))
</dt> <dt>

[Central de Segurança do TechNet](https://technet.microsoft.com/security/)
</dt> </dl>

 

 

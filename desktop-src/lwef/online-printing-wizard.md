---
title: Assistente de impressão online
description: O assistente de impressão online do Windows Vista ajuda os usuários a encomendar impressões de fotos de varejistas de impressão online participantes.
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- Assistente de impressão online
- ícones, assistente de impressão online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8536eea7a51eddb2dbb46d10c9291a60edfdc74e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294046"
---
# <a name="online-printing-wizard"></a>Assistente de impressão online

O assistente de impressão online do Windows Vista ajuda os usuários a encomendar impressões de fotos de varejistas de impressão online participantes. Esse assistente foi projetado para que ele possa ser invocado programaticamente por qualquer aplicativo que queira oferecer aos usuários a capacidade de encomendar impressões de fotos. O assistente de impressão de fotos está disponível no Windows Vista. PIX para Windows

-   [Recursos fornecidos pelo assistente de impressão online](#features-provided-by-the-online-print-wizard)
-   [Formatos de arquivo de fotos com suporte](#supported-photo-file-formats)
-   [Iniciando programaticamente o assistente de impressão online](#programmatically-launching-the-online-print-wizard)
-   [Acessando o ícone do assistente de impressão online](#accessing-the-online-print-wizard-icon)
-   [Propriedades MRU do assistente de impressão online](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a>Recursos fornecidos pelo assistente de impressão online

O assistente de impressão online do Windows Vista permite que os usuários solicitem impressões de uma seleção de revendedores de impressão online participante. Quando invocado, o assistente:

1.  Aceita um arquivo ou lista de arquivos para os quais as impressões devem ser ordenadas.
2.  Recupera automaticamente a lista atual de varejistas de impressão online participantes e permite que o usuário selecione o varejista do qual comprar as impressões de fotos.
3.  Orienta o usuário pelo processo ou pelo pedido de impressões.

Qualquer aplicativo pode se beneficiar dos recursos oferecidos pelo assistente de impressão online do Windows Vista. Um aplicativo precisa apenas passar o arquivo ou arquivos para os quais as impressões serão ordenadas e o assistente orientará o usuário por meio do processo de ordenação.

A figura a seguir mostra o assistente de impressão online do Windows Vista exibindo uma lista de exemplos de varejistas de impressão online participantes.

![o assistente de impressão online do Windows Vista](images/opw.png)

## <a name="supported-photo-file-formats"></a>Formatos de arquivo de fotos com suporte

O assistente de impressão online do Windows Vista oferece suporte a qualquer formato de arquivo de imagem para o qual um codec do Windows Imaging Component (WIC) esteja instalado. O WIC fornece vários codecs padrão, incluindo:

-   BMP (Bitmap)
-   GIF
-   Formato de ícone (ICO)
-   JPEG
-   PNG
-   TIFF
-   Formato de foto do Windows Media

Para obter mais informações sobre os codecs WIC e WIC, consulte [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).

Os formatos de arquivo com suporte de revendedores de impressão online variam de varejista para varejista; é possível que um varejista específico não ofereça suporte a todos os formatos de arquivo suportados pelo assistente de impressão online do Windows Vista. Se o usuário tentar solicitar impressões em um formato que não tenha suporte do varejista selecionado, o assistente de impressão online do Windows Vista notificará o usuário de que o varejista selecionado não oferece suporte ao formato de arquivo enviado.

## <a name="programmatically-launching-the-online-print-wizard"></a>Iniciando programaticamente o assistente de impressão online

Para invocar o assistente de impressão online do Windows Vista, chame a interface [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) com o seguinte CLSID (identificador de classe):


```
CLSID_PublishDropTarget
```



Esse CLSID é definido em ShObjIdl. h e ShObjIdl. idl. Os arquivos a serem processados pelo assistente de impressão online do Windows Vista são especificados em um objeto [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .

O exemplo de código a seguir demonstra como invocar o assistente de impressão online do Windows Vista.


```
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PublishDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



## <a name="accessing-the-online-print-wizard-icon"></a>Acessando o ícone do assistente de impressão online

O assistente de impressão online do Windows Vista exporta um ícone que pode ser acessado e exibido por aplicativos que o chamam. A figura a seguir mostra o ícone do assistente de impressão online do Windows Vista.

![o ícone do assistente de impressão online do Windows Vista](images/opw-icon.png)

O exemplo de código a seguir demonstra como recuperar o índice para o ícone do assistente de impressão online do Windows Vista lendo a propriedade **OPWIcon** .


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;

spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

// Read the icon index from the properties set. 
CComVariant vtIcon;
int nIndex;
hr = spPropsBag->Read(L"OPWIcon", &vtIcon, NULL);

if SUCCEEDED(hr)
{
    nIndex = vtIcon.lVal;
}
```



## <a name="online-print-wizard-mru-properties"></a>Propriedades MRU do assistente de impressão online

O assistente de impressão online do Windows Vista define três propriedades que estão relacionadas ao varejista de impressão online usado mais recentemente (MRU).



| Nome da Propriedade | Valor/função da propriedade                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MRUIcon**   | O índice do ícone para o varejista de impressão online usado mais recentemente pode ser lido com base nesta propriedade.                                                                                                                                                                 |
| **MRUName**   | O nome do varejista de impressão online usado mais recentemente pode ser lido com base nesta propriedade.                                                                                                                                                                               |
| **UseMRU**    | Um valor  ** \_ booliano** de **Variant** VT que indica se o assistente deve ignorar a página de seleção de revendedor de impressão online e apenas usar o revendedor de impressão online usado mais recentemente. Defina essa propriedade como **Variant \_ true** para ignorar a página de seleção de varejista. |



 

O exemplo de código a seguir demonstra como definir a propriedade UseMRU para que o assistente de impressão online do Windows Vista ignore a página de seleção de revendedor de impressão online e selecione automaticamente o varejista usado mais recentemente.


```
// A data object that contains the list of photos to order prints for.
IDataObject* pDataObject;

// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Set the UserMRU property to true to skip retailer selection and use 
// the MRU retailer instead.    
CComQIPtr<IPropertyBag> spPropsBag(spDropTarget);
if(spPropsBag) 
{
    VARIANT varTrue = {0};
    varTrue.vt = VT_BOOL;
    varTrue.boolVal = VARIANT_TRUE;
    spPropsBag->Write(L"UseMRU", &varTrue);
}

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);
```



O exemplo de código a seguir demonstra como ler as propriedades MRUName e MRUIcon.


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;
spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

CComVariant vtMRUName, vtMRUIconIndex;
CComBSTR bstrMRUName;
int nMRUIconIndex;

// Get the MRU name value.
hr = spPropsBag->Read(L"MRUName", &vtMRUName, NULL);
if SUCCEEDED(hr) 
{
    bstrMRUName = vtMRUName.bstrVal;
}

// Get the MRU icon index value.
hr = spPropsBag->Read(L"MRUIcon", &vtMRUIconIndex, NULL);
if SUCCEEDED(hr)
{
    nMRUIconIndex = vtMRUIconIndex.lVal;
}
```



 

 
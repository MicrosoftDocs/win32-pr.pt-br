---
title: Assistente de Impressão Online
description: O Windows Vista Online Printing ajuda os usuários a ordenar impressões de fotos de varejistas de impressão online participantes.
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- Assistente de Impressão Online
- ícones, Assistente de Impressão Online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc402f1fe5853c7a255ea45940d62efcd092c424be6905287315c5cfe5fc7504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975906"
---
# <a name="online-printing-wizard"></a>Assistente de Impressão Online

O Windows Vista Online Printing ajuda os usuários a ordenar impressões de fotos de varejistas de impressão online participantes. Esse assistente foi projetado para que ele possa ser invocado programaticamente por qualquer aplicativo que queira oferecer aos usuários a capacidade de ordenar impressões de fotos. O Assistente de Impressão de Fotos está disponível no Windows Vista. BLOOM para Windows

-   [Recursos fornecidos pelo Assistente de Impressão Online](#features-provided-by-the-online-print-wizard)
-   [Formatos de arquivo de foto com suporte](#supported-photo-file-formats)
-   [Iniciando programaticamente o Assistente de Impressão Online](#programmatically-launching-the-online-print-wizard)
-   [Acessando o ícone do Assistente de Impressão Online](#accessing-the-online-print-wizard-icon)
-   [Propriedades do MRU do Assistente de Impressão Online](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a>Recursos fornecidos pelo Assistente de Impressão Online

O Windows de Impressão Online do Vista permite que os usuários peçam impressões de uma seleção de varejistas de impressão online participantes. Quando invocado, o assistente:

1.  Aceita um arquivo ou uma lista de arquivos para os quais as impressões devem ser ordenadas.
2.  Recupera automaticamente a lista atual de varejistas de impressão online participantes e permite que o usuário selecione o varejista do qual comprar as impressões de fotos.
3.  Orienta o usuário pelo processo ou pela ordenação de impressões.

Qualquer aplicativo pode se beneficiar dos recursos oferecidos pelo assistente de impressão Windows Vista Online. Um aplicativo só precisa passar o arquivo ou arquivos para os quais as impressões serão ordenadas e o assistente orienta o usuário pelo processo de ordenação.

A figura a seguir mostra o assistente Windows impressão online do Vista exibindo uma lista de exemplos de varejistas de impressão online participantes.

![o assistente de impressão online do Windows Vista](images/opw.png)

## <a name="supported-photo-file-formats"></a>Formatos de arquivo de foto com suporte

O Windows de Impressão Online do Vista dá suporte a qualquer formato de arquivo de imagem para o qual um codec do WIC (componente de Windows de imagem) está instalado. O WIC fornece vários codecs padrão, incluindo:

-   BMP (Bitmap)
-   GIF
-   Formato de ícone (ICO)
-   JPEG
-   PNG
-   TIFF
-   Windows Formato de foto de mídia

Para obter mais informações sobre codecs WIC e WIC, [consulte Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).

Os formatos de arquivo com suporte dos varejistas de impressão online variam de varejista para varejista; É possível que um varejista específico não possa dar suporte a todos os formatos de arquivo com suporte pelo Assistente Windows Impressão Online do Vista. Se o usuário tentar solicitar impressões em um formato sem suporte do varejista selecionado, o Assistente de Impressão Online do Windows Vista notifica o usuário de que o varejista selecionado não dá suporte ao formato de arquivo enviado.

## <a name="programmatically-launching-the-online-print-wizard"></a>Iniciando programaticamente o Assistente de Impressão Online

Para invocar o assistente Windows Impressão Online do Vista, chame a interface [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) com o seguinte identificador de classe (CLSID):


```
CLSID_PublishDropTarget
```



Essa CLSID é definida em Shobjidl.h e Shobjidl.idl. Os arquivos a serem processados pelo assistente Windows impressão online do Vista são especificados em um [objeto IDataObject.](/windows/win32/api/objidl/nn-objidl-idataobject)

O exemplo de código a seguir demonstra como invocar o assistente Windows Impressão Online do Vista.


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



## <a name="accessing-the-online-print-wizard-icon"></a>Acessando o ícone do Assistente de Impressão Online

O Windows de Impressão Online do Vista exporta um ícone que pode ser acessado e exibido por aplicativos que o chamam. A figura a seguir mostra o Windows Assistente de Impressão Online do Vista.

![o ícone do assistente de impressão online do Windows Vista](images/opw-icon.png)

O exemplo de código a seguir demonstra como recuperar o índice para o ícone Windows Assistente de Impressão Online do Vista lendo a **propriedade OPWIcon.**


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



## <a name="online-print-wizard-mru-properties"></a>Propriedades do MRU do Assistente de Impressão Online

O Windows de Impressão Online do Vista define três propriedades relacionadas ao varejista de impressão online mru (mru) usado mais recentemente.



| Nome da Propriedade | Valor/função da propriedade                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MRUIcon**   | O índice do ícone para o varejista de impressão online usado mais recentemente pode ser lido nessa propriedade.                                                                                                                                                                 |
| **MRUName**   | O nome do varejista de impressão online usado mais recentemente pode ser lido nessa propriedade.                                                                                                                                                                               |
| **UseMRU**    | Um **valor VARIANT** **VT \_ BOOL** que indica se o assistente deve ignorar a página de seleção do varejista de impressão online e usar apenas o varejista de impressão online usado mais recentemente. De definir essa propriedade como **VARIANT \_ TRUE para** ignorar a página de seleção do varejista. |



 

O exemplo de código a seguir demonstra como definir a propriedade UseMRU para que o Assistente de Impressão Online do Windows Vista ignore a página de seleção do varejista de impressão online e selecione automaticamente o varejista usado mais recentemente.


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



 

 
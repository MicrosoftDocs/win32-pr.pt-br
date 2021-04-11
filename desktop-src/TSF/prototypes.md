---
title: Protótipos
description: Protótipos
ms.assetid: 2b31c01b-d52b-4df5-9cb0-a35286febd3a
keywords:
- TSF (estrutura de serviços de texto), protótipos
- TSF (estrutura de serviços de texto), protótipos
- Referência de TSF, protótipos
- referência para TSF, protótipos
- serviços de texto, protótipos
- Aplicativos habilitados para TSF, protótipos
- protótipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6212461b45d65b73caa77cf21b7591a77ef2a199
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366105"
---
# <a name="prototypes"></a>Protótipos

[ITfContextRenderingMarkup](/windows/desktop/TSF/itfcontextrenderingmarkup), [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup)e [TF \_ RENDERINGMARKUP](/windows/desktop/TSF/tf-renderingmarkup) descritos nesta referência não são definidos em arquivos IDL ou de cabeçalho. Os protótipos a seguir são necessários para serem compatíveis com o compilador MIDL para obter o arquivo de cabeçalho.


```C++
typedef struct
{
    ITfRange *pRange;
    TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;

// 
// IEnumTfRenderingMarkup 
// 
[
  object,
  uuid(8c03d21b-95a7-4ba0-ae1b-7fce12a72930),
  pointer_default(unique)
]
interface IEnumTfRenderingMarkup : IUnknown
{
    HRESULT Clone([out] IEnumTfRenderingMarkup **ppClone);

    HRESULT Next([in] ULONG ulCount,
                 [out, size_is(ulCount), length_is(*pcFetched)] TF_RENDERINGMARKUP *rgMarkup,
                 [out] ULONG *pcFetched);

    HRESULT Reset();

    HRESULT Skip([in] ULONG ulCount);
};

// 
// ITfContextRenderingMarkup 
// 
[
  object,
  uuid(a305b1c0-c776-4523-bda0-7c5a2e0fef10),
  pointer_default(unique)
]
interface ITfContextRenderingMarkup : IUnknown
{
    const DWORD TF_GRM_INCLUDE_PROPERTY = 0x1;

    HRESULT GetRenderingMarkup([in] TfEditCookie ec,
                               [in] DWORD dwFlags,
                               [in] ITfRange *pRangeCover,
                               [out] IEnumTfRenderingMarkup **ppEnum);
                                                           
    HRESULT FindNextRenderingMarkup([in] TfEditCookie ec,
                                    [in] DWORD dwFlags,
                                    [in] ITfRange *pRangeQuery,
                                    [in] TfAnchor tfAnchorQuery,
                                    [out] ITfRange **ppRangeFound,
                                    [out] TF_RENDERINGMARKUP *ptfRenderingMarkup);
};
```



 

 
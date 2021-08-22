---
description: Representa um tablet anexado ao computador.
ms.assetid: 31e11f7d-5610-4c49-9203-2dc322fbef95
title: Interface ITablet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: a0cb98a74758d701e7ab6322567d2a20606380a58fc43676ad5edb136cec999b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712246"
---
# <a name="itablet-interface"></a>Interface ITablet

Representa um tablet anexado ao computador.

## <a name="members"></a>Membros

A interface **ITablet** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **O ITablet** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **interface ITablet** tem esses métodos.



| Método                                                                 | Descrição                                                                           |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**CreateContext**](itablet-createcontext.md)                         | Cria um objeto de contexto que descreve o dispositivo de tablet especificado.<br/>       |
| [**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))                                 | Recupera o objeto [**ITabletCursor**](itabletcursor.md) especificado.<br/>     |
| [**GetCursorCount**](itablet-getcursorcount.md)                       | Recupera o número de objetos de cursor associados ao tablet.<br/>         |
| [**GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md) | Recupera as configurações de contexto padrão para o tablet.<br/>                     |
| [**GetHardwareCaps**](itablet-gethardwarecaps.md)                     | Recupera um valor que representa os recursos do hardware do tablet.<br/> |
| [**GetMaxInputRect**](itablet-getmaxinputrect.md)                     | Recupera um retângulo que representa a área de entrada máxima do tablet.<br/>    |
| [**GetName**](itablet-getname.md)                                     | Recupera uma cadeia de caracteres que contém o nome do dispositivo de tablet.<br/>               |
| [**GetPlugAndPlayId**](itablet-getplugandplayid.md)                   | Recupera uma cadeia de caracteres que contém Plug and Play ID do dispositivo de tablet.<br/>  |
| [**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))               | Recupera os dados de métricas de uma propriedade especificada.<br/>                       |



 

## <a name="remarks"></a>Comentários

Os desenvolvedores não devem usar essa interface.

O código a seguir descreve como a interface **ITablet** é definida.

``` syntax
[
    object,
   uuid(1CB2EFC3-ABC7-4172-8FCB-3BC9CB93E29F),
    pointer_default(unique)
]
interface ITablet : IUnknown
{
    HRESULT GetDefaultContextSettings(
        [out] TABLET_CONTEXT_SETTINGS **ppTCS);

    HRESULT CreateContext(
        [in] HWND hWnd,
        [in, unique] RECT *prcInput,
        [in] DWORD dwOptions,
        [in, unique] TABLET_CONTEXT_SETTINGS *pTCS,
        [in] CONTEXT_ENABLE_TYPE cet,
        [out] ITabletContext **ppCtx,
        [in, out, unique] TABLET_CONTEXT_ID *pTcid,
        [in, out, unique] PACKET_DESCRIPTION **ppPD,
        [in, unique] ITabletEventSink *pSink);

    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetMaxInputRect(
        [out] RECT *prcInput);

    HRESULT GetHardwareCaps(
        [out] DWORD *pdwCaps);

    HRESULT GetPropertyMetrics(
        [in] REFGUID rguid,
        [out] PROPERTY_METRICS *pPM);

    HRESULT GetPlugAndPlayId(
        [out] LPWSTR *ppwszPPId);

    HRESULT GetCursorCount(
        [out] ULONG *pcCurs);

    HRESULT GetCursor(
        [in] ULONG iCur,
        [out] ITabletCursor **ppCur);
};   
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 


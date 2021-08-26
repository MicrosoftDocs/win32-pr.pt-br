---
description: Representa o contexto do Tablet.
ms.assetid: d518c42d-c2f6-4776-bea5-fecdfe48e260
title: Interface ITabletContextP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: da5c26a0a9d7d080a9787fef0b7ba2fdb919e473fd66c989fca478c4ac7d0ac3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883516"
---
# <a name="itabletcontextp-interface"></a>Interface ITabletContextP

Representa o contexto do Tablet.

## <a name="members"></a>Membros

A interface **ITabletContextP** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITabletContextP** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITabletContextP** tem esses métodos.



| Método                                                                                           | Descrição                                                                     |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**IsTopMostHook**](itabletcontextp-istopmosthook.md)                                           | Indica se o contexto do Tablet está na parte superior do gancho.<br/>             |
| [**Post**](itabletcontextp-overlap.md)                                                       | Move um contexto do Tablet para a frente ou para trás da fila de entrada.<br/>      |
| [**TrackInputRect**](itabletcontextp-trackinputrect.md)                                         | Atualiza o Tablet digitalizador para as coordenadas de mapeamento de local de janela.<br/> |
| [**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) | Fornece acesso à memória compartilhada entre threads do Tablet.<br/>             |
| [**UseSharedMemoryCommunications**](itabletcontextp-usesharedmemorycommunications.md)           | Fornece acesso à memória compartilhada entre threads do Tablet.<br/>             |



 

## <a name="remarks"></a>Comentários

Os desenvolvedores não devem usar essa interface.

o [**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) só está disponível no Windows Vista e versões posteriores.

O código a seguir descreve como a interface **ITabletContextP** é definida.

``` syntax
[
    object,
    uuid(22F74D0A-694F-4f47-A5CE-AE08A6409AC8),
    pointer_default(unique)
]
interface ITabletContextP : ITabletContext
{

    HRESULT Overlap([in] BOOL bTop, [out] DWORD *pdwtcid);

    HRESULT GetType([out] CONTEXT_TYPE *pct);

    HRESULT TrackInputRect([out] RECT *prcInput);

    HRESULT IsTopMostHook();

    HRESULT GetEventSink(
        [out] ITabletEventSink **ppSink);

    HRESULT UseSharedMemoryCommunications(
        [in]  DWORD pid,
        [out] DWORD *phEventMoreData,
        [out] DWORD *phEventClientReady,
        [out] DWORD *phMutexAccess,
        [out] DWORD *phFileMapping);

    HRESULT UseNamedSharedMemoryCommunications(
        [in] DWORD pid,
        [in, string] LPCTSTR szSid,
        [in, string] LPCTSTR sdIlSid,
        [out] DWORD *pdwEventMoreDataId,
        [out] DWORD *pdwEventClientReadyId,
        [out] DWORD *pdwMutexAccessId,
        [out] DWORD *pdwFileMappingId);
};
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 


---
description: Expõe rotinas de retorno de chamada para monitorar o processo de pesquisa.
title: Interface IShellFolderSearchableCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3412a01b-d5ea-44e1-819c-f10f81fac391
ms.openlocfilehash: 620acb5d5a3486b721cac3818c57b8392174436f68a304a8788ef62bccae28b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443286"
---
# <a name="ishellfoldersearchablecallback-interface"></a>Interface IShellFolderSearchableCallback

Expõe rotinas de retorno de chamada para monitorar o processo de pesquisa.

## <a name="members"></a>Membros

A interface **IShellFolderSearchableCallback** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IShellFolderSearchableCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IShellFolderSearchableCallback** tem esses métodos.



| Método                                                      | Descrição                                      |
|:------------------------------------------------------------|:-------------------------------------------------|
| [**RunBegin**](ishellfoldersearchablecallback-runbegin.md) | Indica que uma pesquisa foi iniciada.<br/>  |
| [**RunEnd**](ishellfoldersearchablecallback-runend.md)     | Indica que uma pesquisa foi concluída.<br/> |



 

## <a name="remarks"></a>Comentários

Essa interface não está definida em nenhum arquivo de cabeçalho público. Se você optar por implementar essa interface, poderá usar o código C/C++ a seguir para declarar seus métodos.


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchableCallback
DECLARE_INTERFACE_IID_(IShellFolderSearchableCallback, IUnknown, "F98D8294-2BBC-11d2-8DBD-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderSearchableCallback Methods ***

    STDMETHOD(RunBegin)(THIS_ DWORD dwReserved) PURE;
    STDMETHOD(RunEnd)(THIS_ DWORD dwReserved) PURE;
};
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 

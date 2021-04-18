---
description: Inicializa um objeto de serviço do sistema para instalar um objeto ActiveX quando o usuário atual não tem permissão para instalar o objeto.
ms.assetid: 42f7cf83-789b-42ea-bb1a-4b79137188ea
title: Interface IeAxiService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService
api_type:
- COM
api_location: ''
ms.openlocfilehash: 34c4743327b2539616dee6b09c34d9f479aa3303
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755968"
---
# <a name="ieaxiservice-interface"></a>Interface IeAxiService

A interface **IAxiService** Inicializa um objeto de serviço do sistema para instalar um objeto ActiveX quando o usuário atual não tem permissão para instalar o objeto.

A classe [**CIeAxiInstallerService**](cieaxiinstallerservice.md) implementa essa interface.

Essa interface não é declarada em um cabeçalho público. Os aplicativos devem defini-lo por conta própria. O fragmento IDL (Interface Definition Language) a seguir descreve essa interface, incluindo seu IID.

``` syntax
[
    object,
    uuid(E9E92380-9ECD-4982-A0EB-6815A56CCF27),
    pointer_default(unique)
]

interface IeAxiService : IUnknown{

    
    HRESULT Initialize(
            [in]        HWND            hwndParent,
            [in]        DWORD           dwClientPID,
            [in]        BSTR            bstrDesktop,
            [in]        BSTR            bstrClsID,              
            [in]        BSTR            bstrURL,                
            [out]       BSTR *          pbstrNonce,            
            [out]       IUnknown**      ppISyncBrokerInterface  
            );  
 
    HRESULT Cleanup();
};
```

## <a name="members"></a>Membros

A interface **IeAxiService** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IeAxiService** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IeAxiService** tem esses métodos.



| Método                                        | Descrição                                                        |
|:----------------------------------------------|:-------------------------------------------------------------------|
| [**Eliminação**](ieaxiservice-cleanup.md)       | Libera recursos usados pela interface **IeAxiService** .<br/> |
| [**Inicializar**](ieaxiservice-initialize.md) | Verifica e baixa um objeto ActiveX.<br/>                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Business, Windows Vista Enterprise, \[ somente aplicativos de área de trabalho do Windows Vista Ultimate\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService é definido como E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



 


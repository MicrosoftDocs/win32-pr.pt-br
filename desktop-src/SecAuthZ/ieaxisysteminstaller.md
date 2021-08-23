---
description: Instala um objeto ActiveX aplicativo.
ms.assetid: 0eb725a9-ceb8-40e5-808d-ac2b286a48b6
title: Interface IeAxiSystemInstaller
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: fb462c4b4f8fc28d9d00de230dea1bbd3670c4fb6eaa962d59875b4fd9054c8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671006"
---
# <a name="ieaxisysteminstaller-interface"></a>Interface IeAxiSystemInstaller

A interface **IeAxiSystemInstaller** instala um ActiveX objeto .

Essa interface não é declarada em um header público. Os aplicativos devem defini-lo por conta própria. O fragmento IDL (Linguagem de Definição de Interface) a seguir descreve essa interface, incluindo sua IID.

``` syntax
[
    object,
    uuid(a50ea6f8-4764-4299-b309-022b2a8b4d8d),
    
]
interface IeAxiSystemInstaller : IUnknown
{
    
    HRESULT InitializeSystemInstaller(  [in] BSTR bstrUrl,
                                  [in] DWORD dwClientPID,
                                  [in] IUnknown* pCallback,
                                  [out] BSTR * pbstrNonce);
}

```

## <a name="members"></a>Membros

A interface **IeAxiSystemInstaller** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IeAxiSystemInstaller** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IeAxiSystemInstaller** tem esses métodos.



| Método                                                                              | Descrição                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [**InitializeSystemInstaller**](ieaxisysteminstaller-initializesysteminstaller.md) | Instala o objeto ActiveX especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Business, Windows Vista Enterprise, Windows aplicativos de área de trabalho do Vista Ultimate \[\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller é definido como a50ea6f8-4764-4299-b309-022b2a8b4d8d<br/>                   |



 


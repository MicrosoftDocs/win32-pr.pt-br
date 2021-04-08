---
description: Instala um objeto ActiveX.
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
ms.openlocfilehash: 391088a70aa845cd685511f10e4eb6e809dc7fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011623"
---
# <a name="ieaxisysteminstaller-interface"></a>Interface IeAxiSystemInstaller

A interface **IeAxiSystemInstaller** instala um objeto ActiveX.

Essa interface não é declarada em um cabeçalho público. Os aplicativos devem defini-lo por conta própria. O fragmento IDL (Interface Definition Language) a seguir descreve essa interface, incluindo seu IID.

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

A interface **IeAxiSystemInstaller** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IeAxiSystemInstaller** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IeAxiSystemInstaller** tem esses métodos.



| Método                                                                              | Descrição                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [**InitializeSystemInstaller**](ieaxisysteminstaller-initializesysteminstaller.md) | Instala o objeto ActiveX especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Business, Windows Vista Enterprise, \[ somente aplicativos de área de trabalho do Windows Vista Ultimate\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller é definido como a50ea6f8-4764-4299-b309-022b2a8b4d8d<br/>                   |



 


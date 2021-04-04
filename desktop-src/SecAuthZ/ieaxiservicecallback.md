---
description: Chamado pela interface IeAxiSystemInstaller para verificar se um objeto ActiveX pode ser instalado.
ms.assetid: d5cd6263-d07e-4261-9463-b9a06e883f16
title: Interface IeAxiServiceCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3ad276126548ac6d5fdc2c828f722c90b43ad679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837392"
---
# <a name="ieaxiservicecallback-interface"></a>Interface IeAxiServiceCallback

A interface **IeAxiServiceCallback** é chamada pela interface [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) para verificar se um objeto ActiveX pode ser instalado.

A classe [**CIeAxiInstallerService**](cieaxiinstallerservice.md) implementa essa interface.

Essa interface não é declarada em um cabeçalho público. Os aplicativos devem defini-lo por conta própria. O fragmento IDL (Interface Definition Language) a seguir descreve essa interface, incluindo seu IID.

``` syntax
[
    object,
    uuid(1823E7BA-EC36-447a-9B2E-B4912E15AFE7),
    dual,
    nonextensible,
    pointer_default(unique)
]

interface IeAxiServiceCallback : IUnknown
{
    HRESULT VerifyFile(
                       [in] BSTR bstrFileUrl,
                       [out] BSTR * bstrApprovedFileName);
}

```

## <a name="members"></a>Membros

A interface **IeAxiServiceCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IeAxiServiceCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IeAxiServiceCallback** tem esses métodos.



| Método                                                | Descrição                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verificarfile**](ieaxiservicecallback-verifyfile.md) | Executa verificações de segurança no objeto ActiveX especificado e retorna o local onde o arquivo. cab correspondente foi baixado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Business, Windows Vista Enterprise, \[ somente aplicativos de área de trabalho do Windows Vista Ultimate\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiServiceCallback é definido como 1823E7BA-EC36-447A-9B2E-B4912E15AFE7<br/>                   |



 


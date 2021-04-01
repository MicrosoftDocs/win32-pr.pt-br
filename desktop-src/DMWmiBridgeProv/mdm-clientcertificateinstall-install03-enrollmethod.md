---
title: Método EnrollMethod da classe MDM_ClientCertificateInstall_Install03
description: Dispara o dispositivo para iniciar o registro de certificado.
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- Método EnrollMethod
- Método EnrollMethod, classe MDM_ClientCertificateInstall_Install03
- Classe MDM_ClientCertificateInstall_Install03, método EnrollMethod
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03.EnrollMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7903407d5a97f056835e529eb21408bdcbe800ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644934"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a>Método EnrollMethod da \_ classe Install03 do MDM ClientCertificateInstall \_

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Dispara o dispositivo para iniciar o registro de certificado. O dispositivo não notificará o servidor MDM após a conclusão do registro de certificado. O servidor MDM pode consultar o dispositivo posteriormente para descobrir se o novo certificado foi adicionado. Consulte também [**registrar**](/windows/client-management/mdm/clientcertificateinstall-csp).

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Obrigatórios. Dispara o dispositivo para iniciar o registro de certificado. O dispositivo não notificará o servidor MDM após a conclusão do registro de certificado. O servidor MDM pode consultar o dispositivo posteriormente para descobrir se o novo certificado foi adicionado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\Dmmap de \\ MDM \\ cimv2 raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Install03 CLIENTCERTIFICATEINSTALL \_ MDM**](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


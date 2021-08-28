---
title: Método EnrollMethod da MDM_ClientCertificateInstall_Install03 classe
description: Dispara o dispositivo para iniciar o registro de certificado.
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- Método EnrollMethod
- Método EnrollMethod, MDM_ClientCertificateInstall_Install03 classe
- MDM_ClientCertificateInstall_Install03 classe, método EnrollMethod
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
ms.openlocfilehash: 1ddeca621f58015aa3806212c1250aeb43554a51cbb28e15414e779571b9c102
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109396"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a>Método EnrollMethod da classe MDM \_ ClientCertificateInstall \_ Install03

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Dispara o dispositivo para iniciar o registro de certificado. O dispositivo não notificará o servidor MDM depois que o registro de certificado for feito. O servidor MDM pode consultar posteriormente o dispositivo para descobrir se o novo certificado foi adicionado. Consulte também [**Registrar**](/windows/client-management/mdm/clientcertificateinstall-csp).

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Obrigatórios. Dispara o dispositivo para iniciar o registro de certificado. O dispositivo não notificará o servidor MDM depois que o registro de certificado for feito. O servidor MDM pode consultar posteriormente o dispositivo para descobrir se o novo certificado foi adicionado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\Cimv2 \\ mdm \\ dmmap raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MDM \_ ClientCertificateInstall \_ Install03**](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


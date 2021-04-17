---
title: Método HostedInstallMethod da classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: Método para executar uma instalação de um pacote de aplicativo de um local hospedado, como uma unidade local, uma UNC ou uma fonte de dados HTTPS. Consulte também HostedInstall.
ms.assetid: 1ec16315-75ce-4613-804e-6b587c4071d6
keywords:
- Método HostedInstallMethod
- Método HostedInstallMethod, classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01, método HostedInstallMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.HostedInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9597f748a2b5695fd2703f187cfe50db7ad0aa85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753559"
---
# <a name="hostedinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a>Método HostedInstallMethod da classe MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Método para executar uma instalação de um pacote de aplicativo de um local hospedado, como uma unidade local, uma UNC ou uma fonte de dados HTTPS. Consulte também [HostedInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).

## <a name="syntax"></a>Sintaxe


```mof
uint32 HostedInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*parâmetro* \[ no\]
</dt> <dd></dd> </dl>

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

[**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01**](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


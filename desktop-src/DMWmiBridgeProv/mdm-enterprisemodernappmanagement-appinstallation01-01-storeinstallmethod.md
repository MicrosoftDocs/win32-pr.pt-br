---
title: Método StoreInstallMethod da classe MDM_EnterpriseModernAppManagement_AppInstallation01_01 dados
description: Método para executar uma instalação de um aplicativo e uma licença da Windows Store. Consulte também StoreInstall.
ms.assetid: 4f8aff47-ad16-4fe5-85be-7ddb55ddff24
keywords:
- Método StoreInstallMethod
- Método StoreInstallMethod, MDM_EnterpriseModernAppManagement_AppInstallation01_01 classe
- MDM_EnterpriseModernAppManagement_AppInstallation01_01 classe, método StoreInstallMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.StoreInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a8e60134da45982773c0219ade8e0e0f12f37ec9e6d16cd97f4595ae8b507a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084936"
---
# <a name="storeinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a>Método StoreInstallMethod da classe MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Método para executar uma instalação de um aplicativo e uma licença da Windows Store. Consulte também [StoreInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).

## <a name="syntax"></a>Sintaxe


```mof
uint32 StoreInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*param* \[ Em\]
</dt> <dd></dd> </dl>

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

[**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01**](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


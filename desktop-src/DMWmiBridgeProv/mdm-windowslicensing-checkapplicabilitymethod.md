---
title: Método CheckApplicabilityMethod da classe MDM_WindowsLicensing dados
description: Verifica se a chave do produto inserido pode ser usada para uma atualização de edição, ativação ou alteração de uma chave do produto Windows 10 para dispositivos da área de trabalho. Confira também CheckApplicability.
ms.assetid: b28ea397-72dd-4c10-a9fb-53087c3b654c
keywords:
- Método CheckApplicabilityMethod
- Método CheckApplicabilityMethod, MDM_WindowsLicensing classe
- MDM_WindowsLicensing classe, método CheckApplicabilityMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.CheckApplicabilityMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db236e05ffe7b5b6273e7cba594266c31720932b43a7df2de751a0fa66cced5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750146"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a>Método CheckApplicabilityMethod da classe MDM \_ WindowsLicensing

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Verifica se a chave do produto inserido pode ser usada para uma atualização de edição, ativação ou alteração de uma chave do produto Windows 10 para dispositivos da área de trabalho. Confira também [CheckApplicability.](/windows/client-management/mdm/windowslicensing-csp)

## <a name="syntax"></a>Sintaxe


```mof
uint32 CheckApplicabilityMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*param* \[ Em\]
</dt> <dd>

A chave do produto (Product Key).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

TRUE ou FALSE

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

[**MDM \_ WindowsLicensing**](mdm-windowslicensing.md)
</dt> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


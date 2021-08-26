---
title: método doWipeMethod da classe MDM_RemoteWipe
description: Dispara o dispositivo para iniciar o apagamento remoto.
ms.assetid: dc25dc09-6a74-4c08-b452-b1d83085bb41
keywords:
- método doWipeMethod
- método doWipeMethod, classe MDM_RemoteWipe
- Classe MDM_RemoteWipe, método doWipeMethod
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cff9cb831931c96fa8df1b376f96ea4c20b05bafdb12a85dec00b4f505af4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045636"
---
# <a name="dowipemethod-method-of-the-mdm_remotewipe-class"></a>método doWipeMethod da classe MDM \_ RemoteWipe

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Dispara o dispositivo para iniciar o apagamento remoto. Consulte também, [doborracha](/windows/client-management/mdm/remotewipe-csp).

## <a name="syntax"></a>Sintaxe


```mof
uint32 doWipeMethod(
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
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\DMMap de \\ MDM \\ CIMv2 raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_REMOTEWIPE MDM**](mdm-remotewipe.md)
</dt> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


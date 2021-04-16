---
title: Método SetLoadBalancingState da classe Win32_TSSessionDirectory
description: Define o valor para indicar se o servidor participará do balanceamento de carga do agente de Conexão de Área de Trabalho Remota (agente de conexão RD).
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetLoadBalancingState
- Método SetLoadBalancingState Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método SetLoadBalancingState
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetLoadBalancingState
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88142f5a9c87b4af2688e06d2766ac38d7e234c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758092"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a>Método SetLoadBalancingState da classe Win32 \_ TSSessionDirectory

Define o valor para indicar se o servidor participará do balanceamento de carga do agente de Conexão de Área de Trabalho Remota (agente de conexão RD).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Estadovalue* \[ no\]
</dt> <dd>

Tipo: **UInt32**

Indica se o servidor participará do balanceamento de carga do agente de conexão RD.

<dt>

0
</dt> <dd>

O servidor não participará do balanceamento de carga do agente de conexão de área de trabalho remota.

</dd> <dt>

1
</dt> <dd>

O servidor participará do balanceamento de carga do agente de conexão RD.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

O servidor deve ser Unido a um farm no agente de conexão RD.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 


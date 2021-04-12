---
title: Método SetServerWeight da classe Win32_TSSessionDirectory
description: Define o valor de peso do servidor para o balanceamento de carga do agente de Conexão de Área de Trabalho Remota (agente de conexão RD).
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetServerWeight
- Método SetServerWeight Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método SetServerWeight
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetServerWeight
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e8456fa590de0c9d6236f96f3b09c16087d730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455479"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a>Método SetServerWeight da classe Win32 \_ TSSessionDirectory

Define o valor de peso do servidor para o balanceamento de carga do agente de Conexão de Área de Trabalho Remota (agente de conexão RD).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ServerWeightValue* \[ no\]
</dt> <dd>

Tipo: **UInt32**

O valor de peso do servidor. O intervalo válido é de 1 a 10000.

</dd> </dl>

## <a name="remarks"></a>Comentários

Por padrão, na interface do usuário da configuração do Serviços de Área de Trabalho Remota, o valor do peso do servidor é 100. O peso do servidor é relativo. Portanto, se você atribuir a um servidor um valor de 100 e um valor de 200, o servidor com um peso relativo de 200 receberá o dobro do número de sessões.

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

 


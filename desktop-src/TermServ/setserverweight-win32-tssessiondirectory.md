---
title: Método SetServerWeight da classe Win32_TSSessionDirectory classe
description: Define o valor de peso do servidor para o balanceamento de carga Conexão de Área de Trabalho Remota Broker (Agente de Conexão de RD).
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- Método SetServerWeight Serviços de Área de Trabalho Remota
- Método SetServerWeight Serviços de Área de Trabalho Remota , Win32_TSSessionDirectory classe
- Win32_TSSessionDirectory classe Serviços de Área de Trabalho Remota , método SetServerWeight
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
ms.openlocfilehash: 96d8c9af7995f2d42f02075fde8ae43f4b5f5e9a5ccb7d3fa6f4635cb9645464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604625"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a>Método SetServerWeight da classe \_ Win32 TSSessionDirectory

Define o valor de peso do servidor para o balanceamento de carga Conexão de Área de Trabalho Remota Broker (Agente de Conexão de RD).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ServerWeightValue* \[ Em\]
</dt> <dd>

Tipo: **uint32**

O valor de peso do servidor. O intervalo válido é de 1 a 10000.

</dd> </dl>

## <a name="remarks"></a>Comentários

Por padrão, na interface do usuário do Serviços de Área de Trabalho Remota Configuration, o valor de peso do servidor é 100. O peso do servidor é relativo. Portanto, se você atribuir a um servidor um valor de 100 e um valor de 200, o servidor com um peso relativo de 200 receberá duas vezes o número de sessões.

Managed Object Format arquivos (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 


---
title: Método CreateWinstation da classe Win32_TerminalServiceSetting dados
description: Cria uma nova pilha de ouvintes com base na combinação exclusiva de nome do ouvinte e NIC.
ms.assetid: c0a25c22-e0a4-42b1-9c48-c88eebbc55b5
ms.tgt_platform: multiple
keywords:
- Método CreateWinstation Serviços de Área de Trabalho Remota
- Método CreateWinstation Serviços de Área de Trabalho Remota classe Win32_TerminalServiceSetting ,
- Win32_TerminalServiceSetting classe Serviços de Área de Trabalho Remota , método CreateWinstation
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CreateWinstation
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc78266d18b73ee31634a0fc33a244aea3dd9b30d5f6c65c5d646b7aa3da0de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681395"
---
# <a name="createwinstation-method-of-the-win32_terminalservicesetting-class"></a>Método CreateWinstation da classe Win32 \_ TerminalServiceSetting

O **método CreateWinstation** cria uma nova pilha de ouvintes com base na combinação exclusiva de nome do ouvinte e NIC.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CreateWinstation(
  [in] string Name,
  [in] string WinstaDriverName,
  [in] uint32 LanaId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* \[ Em\]
</dt> <dd>

Nome do ouvinte.

</dd> <dt>

*WinstaDriverName* \[ Em\]
</dt> <dd>

O nome do driver de winstation.

</dd> <dt>

*LangId* \[ Em\]
</dt> <dd>

Número do Adaptador de Rede de Área Local (LANG) netBIOS para a NIC.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores.

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 


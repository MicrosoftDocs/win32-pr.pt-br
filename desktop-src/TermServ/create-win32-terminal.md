---
title: Método Create da classe Win32_Terminal
description: Cria um terminal com configurações padrão que podem ser personalizadas usando as propriedades e métodos das \_ classes TerminalSetting do Win32.
ms.assetid: 64c90695-72d4-42be-a37a-89b54c04a78c
ms.tgt_platform: multiple
keywords:
- Criar Serviços de Área de Trabalho Remota do método
- Criar método Serviços de Área de Trabalho Remota, classe Win32_Terminal
- Classe Win32_Terminal Serviços de Área de Trabalho Remota, método Create
topic_type:
- apiref
api_name:
- Win32_Terminal.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f1edfa22893452f81cf4695a50380842fa5c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454788"
---
# <a name="create-method-of-the-win32_terminal-class"></a>Método Create da \_ classe terminal do Win32

O método **Create** cria um terminal com configurações padrão que podem ser personalizadas usando as propriedades e métodos das classes [**\_ TerminalSetting do Win32**](win32-terminalsetting.md) . A função retorna zero em caso de êxito e um erro na falha.

## <a name="syntax"></a>Sintaxe


```mof
uint32 Create(
  [in] string NewTerminalName,
  [in] string Transport,
  [in] string TerminalProtocol
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NewTerminalName* \[ no\]
</dt> <dd>

Nome do terminal.

</dd> <dt>

*Transporte* \[ no\]
</dt> <dd>

Transporte para o terminal. Essa é uma propriedade da classe [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) .

</dd> <dt>

*TerminalProtocol* \[ no\]
</dt> <dd>

Protocolo para o terminal. Essa é uma propriedade da classe [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Terminal do Win32 \_**](win32-terminal.md)
</dt> </dl>

 


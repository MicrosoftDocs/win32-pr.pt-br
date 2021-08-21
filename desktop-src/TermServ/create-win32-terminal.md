---
title: Criar método da classe Win32_Terminal classe
description: Cria um terminal com configurações padrão que podem ser personalizadas usando as propriedades e os métodos das classes Win32 \_ TerminalSetting.
ms.assetid: 64c90695-72d4-42be-a37a-89b54c04a78c
ms.tgt_platform: multiple
keywords:
- Criar método Serviços de Área de Trabalho Remota
- Criar método Serviços de Área de Trabalho Remota , Win32_Terminal classe
- Win32_Terminal classe Serviços de Área de Trabalho Remota , criar método
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
ms.openlocfilehash: 365c706cc657481c80aec48d96a41737f8c209bff5b2d9e72635de316427cd1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118856315"
---
# <a name="create-method-of-the-win32_terminal-class"></a>Criar método da classe Terminal Win32 \_

O **método Create** cria um terminal com configurações padrão que podem ser personalizadas usando as propriedades e os métodos das classes [**Win32 \_ TerminalSetting.**](win32-terminalsetting.md) A função retorna zero em caso de êxito e um erro em caso de falha.

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

*NewTerminalName* \[ Em\]
</dt> <dd>

Nome do terminal.

</dd> <dt>

*Transporte* \[ Em\]
</dt> <dd>

Transporte para o terminal. Essa é uma propriedade da classe [**Win32 \_ TSGeneralSetting.**](win32-tsgeneralsetting.md)

</dd> <dt>

*TerminalProtocol* \[ Em\]
</dt> <dd>

Protocolo para o terminal. Essa é uma propriedade da classe [**Win32 \_ TSGeneralSetting.**](win32-tsgeneralsetting.md)

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

[**Win32 \_ Terminal**](win32-terminal.md)
</dt> </dl>

 


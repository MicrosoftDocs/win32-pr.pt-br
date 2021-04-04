---
title: Classe Win32_TerminalError
description: Representa um erro de terminal.
ms.assetid: d3f622cd-e4ce-4c7e-999e-940b67fd116c
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TerminalError Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TerminalError classe, descrita
topic_type:
- apiref
api_name:
- Win32_TerminalError
- Win32_TerminalError.Description
- Win32_TerminalError.Operation
- Win32_TerminalError.ParameterInfo
- Win32_TerminalError.ProviderName
- Win32_TerminalError.StatusCode
- Win32_TerminalError.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99724badc6c1ca7a2e4168e5c062b4dd1495ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085296"
---
# <a name="win32_terminalerror-class"></a>\_Classe Win32 TerminalError

Representa um erro de terminal.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
class Win32_TerminalError : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string TerminalName;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TerminalError** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TerminalError** tem essas propriedades.

<dl> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualquer cadeia de caracteres definida pelo usuário que descreva um erro ou status operacional.

Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).

</dd> <dt>

**Operação**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Operação que ocorre no momento de uma falha ou anomalia. Normalmente, o WMI define essa propriedade como o nome de uma API COM para o método WMI, como o seguinte: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).

Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Parâmetros envolvidos em um erro ou alteração de status. Por exemplo, se um aplicativo tentar recuperar uma classe que não existe, essa propriedade será definida como o nome da classe incorreta.

Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica o provedor que causa ou relata um erro ou uma alteração de status. Se um provedor não estiver envolvido, essa cadeia de caracteres será definida como "Gerenciamento do Windows".

Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Contém um código de erro ou informações para uma operação. Pode ser qualquer valor definido pelo provedor, mas o valor 0 (zero) geralmente é reservado para indicar êxito. Essa propriedade é herdada de [**\_ \_ NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus).

</dd> <dt>

**Terminalname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do Sin de terminal em que o erro ocorreu.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da cimv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)
</dt> </dl>

 


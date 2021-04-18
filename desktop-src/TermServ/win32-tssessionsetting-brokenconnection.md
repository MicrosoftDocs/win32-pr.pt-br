---
title: Método BrokenConnection da classe Win32_TSSessionSetting (Wtsprotocol. h)
description: Define a propriedade BrokenConnectionAction, que é a ação que o servidor executará se o limite de tempo de sessão for atingido ou se a conexão for interrompida.
ms.assetid: 2422e314-9e1c-4bed-a958-eedd2daeca66
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método BrokenConnection
- Método BrokenConnection Serviços de Área de Trabalho Remota, classe Win32_TSSessionSetting
- Classe Win32_TSSessionSetting Serviços de Área de Trabalho Remota, método BrokenConnection
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.BrokenConnection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90b3f6bada75812b37df014cedadfb4e7ff2e83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788022"
---
# <a name="brokenconnection-method-of-the-win32_tssessionsetting-class"></a>Método BrokenConnection da classe Win32 \_ TSSessionSetting

Define a propriedade **BrokenConnectionAction** , que é a ação que o servidor executará se o limite de tempo de sessão for atingido ou se a conexão for interrompida.

## <a name="syntax"></a>Sintaxe


```mof
uint32 BrokenConnection(
  [in] uint32 BrokenConnectionAction
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*BrokenConnectionAction* \[ no\]
</dt> <dd>

A ação a ser tomada.

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Desconectar** (0)


</dt> <dd>

O usuário está desconectado da sessão.

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminar** (1)


</dt> <dd>

A sessão é excluída permanentemente do servidor.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores. O método retornará um erro se a configuração estiver sob Política de Grupo controle.

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                 |
| parâmetro<br/>                   | <dl> <dt>Wtsprotocol. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSSessionSetting Win32**](win32-tssessionsetting.md)
</dt> </dl>

 


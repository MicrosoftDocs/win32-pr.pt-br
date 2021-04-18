---
title: Método ConnectionSettings da classe Win32_TSClientSetting
description: O método ConnectionSettings define as configurações de sessão que se aplicam ao processo de conexão e logon.
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ConnectionSettings
- Método ConnectionSettings Serviços de Área de Trabalho Remota, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Serviços de Área de Trabalho Remota, método ConnectionSettings
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.ConnectionSettings
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec255f00656684751b750e92d7a3df8290e3573e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499340"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a>Método ConnectionSettings da classe Win32 \_ TSClientSetting

O método **ConnectionSettings** define as configurações de sessão que se aplicam ao processo de conexão e logon.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ConnectionSettings(
  [in] uint32 ConnectClientDrivesAtLogon,
  [in] uint32 ConnectPrinterAtLogon,
  [in] uint32 DefaultToClientPrinter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ConnectClientDrivesAtLogon* \[ no\]
</dt> <dd>

Sinalizador habilitando ou desabilitando a propriedade **ConnectClientDrivesAtLogon** que especifica se as unidades do cliente são conectadas automaticamente durante o procedimento de logon.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

As unidades do cliente não são conectadas automaticamente.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

As unidades do cliente são conectadas automaticamente.

</dd> </dl> </dd> <dt>

*ConnectPrinterAtLogon* \[ no\]
</dt> <dd>

Sinalizador habilitando ou desabilitando a propriedade **ConnectPrinterAtLogon** , que especifica se todas as impressoras de cliente locais mapeadas são automaticamente conectadas durante o procedimento de logon.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Todas as impressoras locais mapeadas não são conectadas automaticamente.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Todas as impressoras locais mapeadas são conectadas automaticamente.

</dd> </dl> </dd> <dt>

*DefaultToClientPrinter* \[ no\]
</dt> <dd>

Sinalizador habilitando ou desabilitando a propriedade **DefaultToClientPrinter** que especifica se os trabalhos de impressão são enviados automaticamente para a impressora local do cliente.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Os trabalhos de impressão não são enviados automaticamente.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Os trabalhos de impressão são enviados automaticamente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores. O método retornará um erro se as configurações de conexão do usuário forem substituídas pelo servidor.

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

[**\_TSClientSetting Win32**](win32-tsclientsetting.md)
</dt> </dl>

 


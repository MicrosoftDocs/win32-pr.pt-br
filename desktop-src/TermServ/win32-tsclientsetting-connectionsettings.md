---
title: Método ConnectionSettings da classe Win32_TSClientSetting classe
description: O método ConnectionSettings define as configurações de sessão que se aplicam ao processo de conexão e logon.
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- Método ConnectionSettings Serviços de Área de Trabalho Remota
- Método ConnectionSettings Serviços de Área de Trabalho Remota , Win32_TSClientSetting classe
- Win32_TSClientSetting classe Serviços de Área de Trabalho Remota , método ConnectionSettings
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
ms.openlocfilehash: e3f48a93959b1e86eb77f6ab0fbfab444444ca1c077835e1c28330d34ed66c87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656166"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a>Método ConnectionSettings da classe \_ Win32 TSClientSetting

O **método ConnectionSettings** define as configurações de sessão que se aplicam ao processo de conexão e logon.

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

*ConnectClientDrivesAtLogon* \[ Em\]
</dt> <dd>

Sinalizar a habilitação ou desabilitação da propriedade **ConnectClientDrivesAtLogon,** que especifica se as unidades do cliente são conectadas automaticamente durante o procedimento de logon.

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

*ConnectPrinterAtLogon* \[ Em\]
</dt> <dd>

Sinalizar a habilitação ou desabilitação da propriedade **ConnectPrinterAtLogon,** que especifica se todas as impressoras cliente locais mapeadas são conectadas automaticamente durante o procedimento de logon.

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

*DefaultToClientPrinter* \[ Em\]
</dt> <dd>

Sinalizar a habilitação ou desabilitação da propriedade **DefaultToClientPrinter,** que especifica se os trabalhos de impressão são enviados automaticamente para a impressora local do cliente.

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

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores. O método retornará um erro se as configurações de conexão do usuário são substituídos pelo servidor.

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

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 


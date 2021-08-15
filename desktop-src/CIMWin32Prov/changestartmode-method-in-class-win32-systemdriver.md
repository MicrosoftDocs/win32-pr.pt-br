---
description: Modifica o modo de início de um \_ serviço do SystemDriver Win32.
ms.assetid: 34f4e0ac-d8a0-4be7-8c84-0252e50db441
ms.tgt_platform: multiple
title: Método ChangeStartMode da classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e2067ae7da8a6f112671237ebc7f77dd26644c5e0b2fa0b77a443c160468581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959125"
---
# <a name="changestartmode-method-of-the-win32_systemdriver-class"></a>Método ChangeStartMode da \_ classe SystemDriver Win32

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica o modo de início de um serviço do [**\_ SystemDriver Win32**](win32-systemdriver.md) .

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartMode* \[ no\]
</dt> <dd>

modo de início do serviço base de Windows.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicialização inicial** ("inicialização")


</dt> <dd>

Driver de dispositivo iniciado pelo carregador do sistema operacional. Esse valor só é válido para serviços do driver.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")


</dt> <dd>

Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional. Esse valor só é válido para serviços do driver.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Início automático** ("automático")


</dt> <dd>

Serviço a ser iniciado automaticamente pelo gerenciador de controle de serviço durante a inicialização do sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Início da demanda** ("manual")


</dt> <dd>

Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-systemdriver.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("desabilitado")


</dt> <dd>

Serviço que não pode mais ser iniciado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) se o serviço tiver sido modificado com êxito, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Acesso negado** (2)
</dt> <dt>

**Serviços dependentes em execução** (3)
</dt> <dt>

**Controle de serviço inválido** (4)
</dt> <dt>

O **serviço não pode aceitar o controle** (5)
</dt> <dt>

**Serviço não ativo** (6)
</dt> <dt>

**Tempo limite da solicitação de serviço** (7)
</dt> <dt>

**Falha desconhecida** (8)
</dt> <dt>

**Caminho não encontrado** (9)
</dt> <dt>

**Serviço já em execução** (10)
</dt> <dt>

**Banco de dados de serviço bloqueado** (11)
</dt> <dt>

**Dependência de serviço excluída** (12)
</dt> <dt>

**Falha de dependência de serviço** (13)
</dt> <dt>

**Serviço desabilitado** (14)
</dt> <dt>

**Falha no logon do serviço** (15)
</dt> <dt>

**Serviço marcado para exclusão** (16)
</dt> <dt>

**Serviço sem thread** (17)
</dt> <dt>

**Dependência circular de status** (18)
</dt> <dt>

**Nome duplicado de status** (19)
</dt> <dt>

**Nome inválido do status** (20)
</dt> <dt>

**Parâmetro de status inválido** (21)
</dt> <dt>

**Conta de serviço inválida de status** (22)
</dt> <dt>

O **serviço de status existe** (23)
</dt> <dt>

**Serviço já pausado** (24)
</dt> <dt>

**Outro** (25 4294967295)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Systemdrive do Win32 \_**](win32-systemdriver.md)
</dt> </dl>

 


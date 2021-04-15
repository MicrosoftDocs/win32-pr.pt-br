---
title: Método ChangeRole da classe Win32_TSLicenseServer
description: Altera o escopo de descoberta do servidor de licença Área de Trabalho Remota. O escopo de descoberta determina quais servidores de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) na rede podem descobrir automaticamente o servidor de licença.
ms.assetid: 3d98fd8a-4ade-489f-8edd-5df1227f15cd
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ChangeRole
- Método ChangeRole Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método ChangeRole
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ChangeRole
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9746b856c74e9603751fe85bb861e2b6869f03a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454839"
---
# <a name="changerole-method-of-the-win32_tslicenseserver-class"></a>Método ChangeRole da classe Win32 \_ TSLicenseServer

Altera o escopo de descoberta do servidor de licença Área de Trabalho Remota. O escopo de descoberta determina quais servidores de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) na rede podem descobrir automaticamente o servidor de licença.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ChangeRole(
  [in] uint32 ServerRole
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ServerRole* \[ no\]
</dt> <dd>

Escopo de descoberta para o servidor de licença Área de Trabalho Remota. Você pode definir um dos valores a seguir.

<dt>

0
</dt> <dd>

Host da Sessão RD servidores no mesmo grupo de trabalho podem descobrir o servidor de licença.

</dd> <dt>

1
</dt> <dd>

Host da Sessão RD servidores no mesmo domínio podem descobrir o servidor de licença. Você deve estar conectado como um administrador de domínio para definir esse valor.

</dd> <dt>

2
</dt> <dd>

Host da Sessão RD servidores de vários domínios na mesma floresta podem descobrir o servidor de licença. Você deve estar conectado como um administrador corporativo para definir esse valor.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 


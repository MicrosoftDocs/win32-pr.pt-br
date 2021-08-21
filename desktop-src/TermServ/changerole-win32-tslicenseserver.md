---
title: Método ChangeRole da Win32_TSLicenseServer classe
description: Altera o escopo de descoberta do servidor Área de Trabalho Remota licença. O escopo de descoberta determina quais Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) na rede podem descobrir automaticamente o servidor de licença.
ms.assetid: 3d98fd8a-4ade-489f-8edd-5df1227f15cd
ms.tgt_platform: multiple
keywords:
- Método ChangeRole Serviços de Área de Trabalho Remota
- Classe Serviços de Área de Trabalho Remota , Win32_TSLicenseServer ChangeRole
- Win32_TSLicenseServer classe Serviços de Área de Trabalho Remota , método ChangeRole
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
ms.openlocfilehash: f010fc1c8d31382040d79bd811e4a472af4269d503d2810e44320717ebbc5e35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575076"
---
# <a name="changerole-method-of-the-win32_tslicenseserver-class"></a>Método ChangeRole da classe \_ Win32 TSLicenseServer

Altera o escopo de descoberta do servidor Área de Trabalho Remota licença. O escopo de descoberta determina quais Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) na rede podem descobrir automaticamente o servidor de licença.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ChangeRole(
  [in] uint32 ServerRole
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ServerRole* \[ Em\]
</dt> <dd>

Escopo de descoberta do servidor Área de Trabalho Remota licença. Você pode definir um dos valores a seguir.

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

Host da Sessão RD servidores de vários domínios na mesma floresta podem descobrir o servidor de licença. Você deve estar conectado como administrador corporativo para definir esse valor.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 


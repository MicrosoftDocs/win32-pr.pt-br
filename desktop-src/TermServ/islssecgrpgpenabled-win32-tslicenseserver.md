---
title: Método IsLSSecGrpGPEnabled da classe Win32_TSLicenseServer
description: Recupera se o grupo de segurança do servidor de licenças \ 0034; \ 0034; a configuração de política de grupo está habilitada no servidor de licença Área de Trabalho Remota.
ms.assetid: 715b619b-f082-4fed-ac4c-70d5e286e37c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método IsLSSecGrpGPEnabled
- Método IsLSSecGrpGPEnabled Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método IsLSSecGrpGPEnabled
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSSecGrpGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 688843106583ea0ca32a3cc8ac7142d51aac737ad6722ab4ef95621b63b66eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138359"
---
# <a name="islssecgrpgpenabled-method-of-the-win32_tslicenseserver-class"></a>Método IsLSSecGrpGPEnabled da classe Win32 \_ TSLicenseServer

Recupera se a configuração da política de grupo "grupo de segurança do servidor de licenças" está habilitada no servidor de licença Área de Trabalho Remota.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsLSSecGrpGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Habilitado* \[ fora\]
</dt> <dd>

Valor booliano que indica se a configuração de política "grupo de segurança de servidor de licenças" está habilitada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

A configuração de política "grupo de segurança de servidor de licenças" permite que você especifique os servidores de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) que têm permissão para contatar o servidor de licença para obter Serviços de Área de Trabalho Remota CALs (licenças de acesso para cliente). Se a configuração de política estiver habilitada no servidor de licença, o servidor responderá apenas a solicitações de RDS CAL de Host da Sessão RD servidores cujas contas de computador são membros do grupo local computadores Terminal Server no servidor de licença.

A configuração de política está localizada no seguinte nó do editor de diretiva de grupo local:

configuração do computador \\ Modelos Administrativos \\ Windows componentes \\ \\ licenciamento TS serviços de Terminal

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 


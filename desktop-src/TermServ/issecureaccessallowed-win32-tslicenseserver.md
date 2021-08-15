---
title: Método IsSecureAccessAllowed da classe Win32_TSLicenseServer
description: Recupera se um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) tem permissão para solicitar Serviços de Área de Trabalho Remota licenças de acesso para cliente (RDS \ 160; CALs) do servidor de licença Área de Trabalho Remota.
ms.assetid: b9124808-79be-4b94-b12b-f093d5e8195a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método IsSecureAccessAllowed
- Método IsSecureAccessAllowed Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método IsSecureAccessAllowed
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsSecureAccessAllowed
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6109eb363459432d50d54eb8521f0f23bb54a0836c82f92af20a5b83b64f1d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351348"
---
# <a name="issecureaccessallowed-method-of-the-win32_tslicenseserver-class"></a>Método IsSecureAccessAllowed da classe Win32 \_ TSLicenseServer

Recupera se um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) tem permissão para solicitar Serviços de Área de Trabalho Remota CALs (licenças de acesso para cliente) do servidor de licença Área de Trabalho Remota.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsSecureAccessAllowed(
  [in]  string  tsname,
  [out] boolean Allowed
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tsname* \[ no\]
</dt> <dd>

Nome do servidor de Host da Sessão RD.

</dd> <dt>

*Permitido* \[ fora\]
</dt> <dd>

Valor booliano que indica se o servidor de Host da Sessão RD tem permissão para solicitar RDS CALs do servidor de licença.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

O valor retornado é baseado na configuração da política de grupo "grupo de segurança do servidor de licenças" e na associação ao grupo local Terminal Server computadores no servidor de licença Área de Trabalho Remota.

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
</dt> <dt>

[**IsLSSecGrpGPEnabled**](islssecgrpgpenabled-win32-tslicenseserver.md)
</dt> </dl>

 


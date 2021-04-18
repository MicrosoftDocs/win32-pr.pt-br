---
title: Método IsLSinTSLSGroup da classe Win32_TSLicenseServer
description: Recupera se o servidor de licença Área de Trabalho Remota é membro do grupo de servidores de licença Área de Trabalho Remota em um controlador de domínio em um determinado domínio.
ms.assetid: a6ad7f09-8972-47d4-8b3b-cd129b400ea8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método IsLSinTSLSGroup
- Método IsLSinTSLSGroup Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método IsLSinTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSinTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de3577e4632167612b4d71841501a2a2845203a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756965"
---
# <a name="islsintslsgroup-method-of-the-win32_tslicenseserver-class"></a>Método IsLSinTSLSGroup da classe Win32 \_ TSLicenseServer

Recupera se o servidor de licença Área de Trabalho Remota é membro do grupo de servidores de licença Área de Trabalho Remota em um controlador de domínio em um determinado domínio.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsLSinTSLSGroup(
  [in]  string  Domain,
  [out] boolean IsMember
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Domínio* \[ do no\]
</dt> <dd>

O nome de domínio.

</dd> <dt>

*IsMember* \[ fora\]
</dt> <dd>

Valor booliano que indica se o servidor de licença é membro do grupo de servidores de licença Área de Trabalho Remota no domínio.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

Se nenhum nome de domínio for fornecido, um controlador de domínio no mesmo domínio que o servidor de licença será consultado.

O servidor de licença deve ser membro do grupo de servidores de licença Área de Trabalho Remota se o servidor estiver configurado para usar o escopo de descoberta de domínio ou floresta. Se o servidor de licença não for membro deste grupo, o rastreamento de licença por usuário e os relatórios não funcionarão.

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
</dt> <dt>

[**AddLStoTSLSGroup**](addlstotslsgroup-win32-tslicenseserver.md)
</dt> <dt>

[**RemoveLSfromTSLSGroup**](removelsfromtslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 


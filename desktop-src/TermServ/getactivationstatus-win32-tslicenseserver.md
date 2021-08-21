---
title: Método GetActivationStatus da classe Win32_TSLicenseServer
description: Recupera o status de ativação atual do servidor de licença Área de Trabalho Remota.
ms.assetid: 1148ffc5-33c1-41f1-b477-78a5293333d1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetActivationStatus
- Método GetActivationStatus Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método GetActivationStatus
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.GetActivationStatus
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d79daa4c73e95eded95f3c7760eef43f0a01683059cc4974506e7b50f291ca1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130765"
---
# <a name="getactivationstatus-method-of-the-win32_tslicenseserver-class"></a>Método GetActivationStatus da classe Win32 \_ TSLicenseServer

Recupera o status de ativação atual do servidor de licença Área de Trabalho Remota.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetActivationStatus(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ActivationStatus* \[ fora\]
</dt> <dd>

O status de ativação retornado pode ser um dos seguintes.

<dt>

0
</dt> <dd>

O servidor de licença Área de Trabalho Remota está ativado.

</dd> <dt>

1
</dt> <dd>

O servidor de licença Área de Trabalho Remota não está ativado.

</dd> <dt>

2
</dt> <dd>

Ocorreu um erro desconhecido. Não é conhecido se o servidor de licença Área de Trabalho Remota está ativado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

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

 


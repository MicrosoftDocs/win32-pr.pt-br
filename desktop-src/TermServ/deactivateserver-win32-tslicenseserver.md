---
title: Método DeactivateServer da classe Win32_TSLicenseServer
description: Desativa o servidor de licença Área de Trabalho Remota usando um código de confirmação que é recebido pelo telefone.
ms.assetid: 84e069b7-9a4f-4843-b656-839f936ac727
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DeactivateServer
- Método DeactivateServer Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método DeactivateServer
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.DeactivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b851a8d8049c9194bce163afc4b7bad5d4aa15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918080"
---
# <a name="deactivateserver-method-of-the-win32_tslicenseserver-class"></a>Método DeactivateServer da classe Win32 \_ TSLicenseServer

Desativa o servidor de licença Área de Trabalho Remota usando um código de confirmação que é recebido pelo telefone.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DeactivateServer(
  [in]  string sConfirmCode,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sConfirmCode* \[ no\]
</dt> <dd>

Código de confirmação.

</dd> <dt>

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

Erro desconhecido. Não é conhecido se o servidor de licença Serviços de Área de Trabalho Remota está ativado.

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

 


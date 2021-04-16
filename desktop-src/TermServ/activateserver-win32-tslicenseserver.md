---
title: Método ActivateServer da classe Win32_TSLicenseServer
description: Ativa o Área de Trabalho Remota servidor de licença usando um identificador de servidor de licença Área de Trabalho Remota que é obtido pelo telefone ou pela Internet.
ms.assetid: 628e87f0-600e-404d-a0b4-35f1570b4fc0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ActivateServer
- Método ActivateServer Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método ActivateServer
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19db0df0ca9b0bf41fe692ba07fe605dc1e8d5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779282"
---
# <a name="activateserver-method-of-the-win32_tslicenseserver-class"></a>Método ActivateServer da classe Win32 \_ TSLicenseServer

Ativa o Área de Trabalho Remota servidor de licença usando um identificador de servidor de licença Área de Trabalho Remota que é obtido pelo telefone ou pela Internet.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ActivateServer(
  [in]  string sLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sLicenseServerId* \[ no\]
</dt> <dd>

Área de Trabalho Remota ID do servidor de licença que foi obtida pelo telefone ou pela Internet. O parâmetro *sLicenseServerId* é uma cadeia de caracteres alfanumérica de 35 caracteres que não pode incluir hifens.

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

Erro desconhecido. Não é conhecido se o servidor de licença Área de Trabalho Remota está ativado.

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

 


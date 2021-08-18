---
title: Método ActivateServer da Win32_TSLicenseServer classe
description: Ativa o servidor Área de Trabalho Remota licença usando um identificador Área de Trabalho Remota do servidor de licenças que é obtido pelo telefone ou pela Internet.
ms.assetid: 628e87f0-600e-404d-a0b4-35f1570b4fc0
ms.tgt_platform: multiple
keywords:
- Método ActivateServer Serviços de Área de Trabalho Remota
- O método ActivateServer Serviços de Área de Trabalho Remota classe Win32_TSLicenseServer ,
- Win32_TSLicenseServer classe Serviços de Área de Trabalho Remota , método ActivateServer
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
ms.openlocfilehash: 86ba3e231da50c9103361b2cf22cbd44d7311a26a4ea36f9a32185ed0c32d408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872066"
---
# <a name="activateserver-method-of-the-win32_tslicenseserver-class"></a>Método ActivateServer da classe \_ Win32 TSLicenseServer

Ativa o servidor Área de Trabalho Remota licença usando um identificador Área de Trabalho Remota do servidor de licenças que é obtido pelo telefone ou pela Internet.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ActivateServer(
  [in]  string sLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sLicenseServerId* \[ Em\]
</dt> <dd>

Área de Trabalho Remota ID do servidor de licença que foi obtida pelo telefone ou pela Internet. O *parâmetro sLicenseServerId* é uma cadeia de caracteres alfanumérico de 35 caracteres que não pode incluir hifens.

</dd> <dt>

*ActivationStatus* \[ out\]
</dt> <dd>

O status de ativação retornado pode ser um dos seguintes.

<dt>

0
</dt> <dd>

O Área de Trabalho Remota de licença está ativado.

</dd> <dt>

1
</dt> <dd>

O Área de Trabalho Remota de licença não está ativado.

</dd> <dt>

2
</dt> <dd>

Ocorreu um erro desconhecido. Não se sabe se o servidor Área de Trabalho Remota licença está ativado.

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

 


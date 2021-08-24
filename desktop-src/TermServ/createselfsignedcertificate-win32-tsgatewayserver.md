---
title: Método CreateSelfSignedCertificate da classe Win32_TSGatewayServer
description: Cria um certificado auto-assinado e retorna o hash do certificado como um \ 0034;out \ 0034; Parâmetro.
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- Método CreateSelfSignedCertificate Serviços de Área de Trabalho Remota
- Método CreateSelfSignedCertificate Serviços de Área de Trabalho Remota , Win32_TSGatewayServer classe
- Win32_TSGatewayServer classe Serviços de Área de Trabalho Remota , método CreateSelfSignedCertificate
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.CreateSelfSignedCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 200b08da8d5eea9f31405a357650384081c407df4eb76820cd47a111e6b66aab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139049"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a>Método CreateSelfSignedCertificate da classe \_ TSGatewayServer do Win32

Cria um certificado auto-assinado e retorna o hash do certificado como um parâmetro "out". Além disso, adiciona o texto "TS GATEWAY SELF SIGNED CERTIFICATE" à propriedade de contexto do certificado para que o certificado seja reconhecido como um certificado Área de Trabalho Remota Gateway de Área de Trabalho Remota \_ \_ \_ \_ (Gateway de RD). Esse método usa um contêiner de chave específico do Gateway de Área de Trabalho Digital para criar o certificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SubjectName* \[ Em\]
</dt> <dd>

Nome da assunto do certificado auto-assinado.

</dd> <dt>

*CertHash* \[ out\]
</dt> <dd>

O hash do certificado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSGatewayServer**](win32-tsgatewayserver.md)
</dt> </dl>

 


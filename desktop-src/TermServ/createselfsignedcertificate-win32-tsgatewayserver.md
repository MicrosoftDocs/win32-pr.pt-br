---
title: Método CreateSelfSignedCertificate da classe Win32_TSGatewayServer
description: Cria um certificado autoassinado e retorna o hash de certificado como um \ 0034; out \ 0034; meter.
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CreateSelfSignedCertificate
- Método CreateSelfSignedCertificate Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServer
- Classe Win32_TSGatewayServer Serviços de Área de Trabalho Remota, método CreateSelfSignedCertificate
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
ms.openlocfilehash: 4258566856a5fbc277053b65afe972751855d831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454787"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a>Método CreateSelfSignedCertificate da classe Win32 \_ TSGatewayServer

Cria um certificado autoassinado e retorna o hash de certificado como um parâmetro "out". Além disso, o adiciona o texto \_ " \_ \_ certificado autoassinado de Gateway TS \_ " à propriedade de contexto de certificado para que o certificado seja reconhecido como um certificado de gateway de área de trabalho remota (gateway de área de trabalho remota). Esse método usa um contêiner de chave específico do gateway de área de trabalho remota para criar o certificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SubjectName* \[ no\]
</dt> <dd>

Nome da entidade do certificado autoassinado.

</dd> <dt>

*CertHash* \[ fora\]
</dt> <dd>

O hash do certificado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TS. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSGatewayServer Win32**](win32-tsgatewayserver.md)
</dt> </dl>

 


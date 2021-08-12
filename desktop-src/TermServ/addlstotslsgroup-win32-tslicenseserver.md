---
title: Método AddLStoTSLSGroup da classe Win32_TSLicenseServer
description: Adiciona o Área de Trabalho Remota de licença do Conexão de Área de Trabalho Remota Broker (Agente de Conexão RD) em um controlador de domínio no mesmo domínio que o Área de Trabalho Remota de licença.
ms.assetid: 65c6b7cf-324a-44f1-8dfc-40e35ed45d4f
ms.tgt_platform: multiple
keywords:
- Método AddLStoTSLSGroup Serviços de Área de Trabalho Remota
- Método AddLStoTSLSGroup Serviços de Área de Trabalho Remota , Win32_TSLicenseServer classe
- Win32_TSLicenseServer classe Serviços de Área de Trabalho Remota , método AddLStoTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.AddLStoTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf3d0464b42159ca1827caf579e21982c08d066495cd664ec1adfcaa883a4b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610401"
---
# <a name="addlstotslsgroup-method-of-the-win32_tslicenseserver-class"></a>Método AddLStoTSLSGroup da classe \_ Win32 TSLicenseServer

Adiciona o Área de Trabalho Remota de licença do Conexão de Área de Trabalho Remota Broker (Agente de Conexão RD) em um controlador de domínio no mesmo domínio que o Área de Trabalho Remota de licença.

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddLStoTSLSGroup();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores de Domínio para chamar esse método.

O servidor de licença deverá ser membro do grupo Área de Trabalho Remota servidores de licença se o servidor estiver configurado para usar o escopo de descoberta de domínio ou floresta.

Managed Object Format arquivos (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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
</dt> <dt>

[**IsLSinTSLSGroup**](islsintslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 


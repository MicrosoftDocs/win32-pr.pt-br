---
title: Método UnpublishLS da classe Win32_TSLicenseServer
description: Cancelar a publicação de um servidor de licença Área de Trabalho Remota do Active Directory Domain Services.
ms.assetid: 275854e2-85f6-4142-8bce-8d633bfcff7d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método UnpublishLS
- Método UnpublishLS Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método UnpublishLS
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.UnpublishLS
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4990488dba9610dc307878f09fdcf2faab6b61b452aebe9860668aee7d59111a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868996"
---
# <a name="unpublishls-method-of-the-win32_tslicenseserver-class"></a>Método UnpublishLS da classe Win32 \_ TSLicenseServer

Cancelar a publicação de um servidor de licença Área de Trabalho Remota do Active Directory Domain Services.

## <a name="syntax"></a>Sintaxe


```mof
uint32 UnpublishLS();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Para chamar esse método, você deve estar conectado como um administrador corporativo à floresta na qual o servidor de licença é membro.

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

 


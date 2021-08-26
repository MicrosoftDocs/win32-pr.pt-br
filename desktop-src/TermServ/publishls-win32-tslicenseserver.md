---
title: Método PublishLS da Win32_TSLicenseServer classe
description: Publica o servidor Área de Trabalho Remota licença do Active Directory Domain Services.
ms.assetid: 726d5dec-e438-455e-adb8-56d646d65d13
ms.tgt_platform: multiple
keywords:
- Método PublishLS Serviços de Área de Trabalho Remota
- Método PublishLS Serviços de Área de Trabalho Remota , Win32_TSLicenseServer classe
- Win32_TSLicenseServer classe Serviços de Área de Trabalho Remota , método PublishLS
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.PublishLS
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5559fc41e08535142642c64658234902aea22d2a47e6b43add30427fdaec0778
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988826"
---
# <a name="publishls-method-of-the-win32_tslicenseserver-class"></a>Método PublishLS da classe \_ Win32 TSLicenseServer

Publica o servidor Área de Trabalho Remota licença do Active Directory Domain Services.

## <a name="syntax"></a>Sintaxe


```mof
uint32 PublishLS();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Para chamar esse método, você deve estar conectado como administrador corporativo à floresta na qual o servidor de licenças é membro.

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

 


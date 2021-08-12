---
title: Registrando o provedor de serviços
description: Registrando o provedor de serviços
ms.assetid: 556d6519-bc24-446b-a360-e3d83b40d541
keywords:
- Windows Mídia Gerenciador de Dispositivos, registrando provedores de serviços
- Gerenciador de Dispositivos, registrando provedores de serviços
- guia de programação, registrando provedores de serviços
- provedores de serviços, registrando provedores de serviços
- criando provedores de serviços, registrando provedores de serviços
- registrando provedores de serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f480fff04d34cf671bdc37e3bcded92c73f20d31d2fb67e4d6e41593a724d392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584276"
---
# <a name="registering-the-service-provider"></a>Registrando o provedor de serviços

Além de ser registrado como um objeto COM, um provedor de serviços deve ser registrado como um plug-in para Windows mídia Gerenciador de Dispositivos. Para se registrar, um provedor de serviços deve criar a seguinte chave do Registro:

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Media Device Manager\Plugins\SP\<             `

Nessa chave, < *nome do provedor* de serviços > é o nome da sua DLL; por exemplo, o provedor de serviços de exemplo usa MsHDSP. A chave ProgID deve ter um valor de cadeia de caracteres que corresponda ao CLSID do seu provedor de serviços. Por exemplo, o provedor de serviços de exemplo tem o valor "MDServiceProviderHD.MDServiceProviderHD".

A implementação do provedor de serviços de exemplo de DLLRegisterServer no Mdsp.cpp adiciona essa chave do Registro quando você registra a DLL do provedor de serviços de exemplo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um provedor de serviços**](creating-a-service-provider.md)
</dt> </dl>

 

 





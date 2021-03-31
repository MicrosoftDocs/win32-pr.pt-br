---
title: Registrando o provedor de serviços
description: Registrando o provedor de serviços
ms.assetid: 556d6519-bc24-446b-a360-e3d83b40d541
keywords:
- Windows Media Gerenciador de Dispositivos, registrando provedores de serviço
- Gerenciador de Dispositivos, registrando provedores de serviço
- Guia de programação, registrando provedores de serviço
- provedores de serviços, registrando provedores de serviços
- criando provedores de serviços, registrando provedores de serviços
- registrando provedores de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1226b724b06990fc1e000a522e3a61672789cf3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005056"
---
# <a name="registering-the-service-provider"></a>Registrando o provedor de serviços

Além de serem registrados como um objeto COM, um provedor de serviços deve ser registrado como um plug-in no Windows Media Gerenciador de Dispositivos. Para se registrar, um provedor de serviços deve criar a seguinte chave do registro:

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Media Device Manager\Plugins\SP\<             `

Nessa chave, < *seu nome de provedor de serviço* > é o nome da sua dll; por exemplo, o provedor de serviços de exemplo usa MsHDSP. A chave ProgID deve ter um valor de cadeia de caracteres que corresponda ao CLSID do seu provedor de serviços. Por exemplo, o provedor de serviços de exemplo tem o valor "MDServiceProviderHD. MDServiceProviderHD".

A implementação do provedor de serviço de exemplo DLLRegisterServer em MDSP. cpp adiciona essa chave do registro quando você registra a DLL do provedor de serviço de exemplo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um provedor de serviços**](creating-a-service-provider.md)
</dt> </dl>

 

 





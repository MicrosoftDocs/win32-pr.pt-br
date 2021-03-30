---
title: Instalando um método EAP
description: Siga as instruções abaixo para instalar um método EAP implementado pelo usuário em um computador cliente que executa o EAPHost.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93e7796c216b5f60b7a46768ed9db9ca913482d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640846"
---
# <a name="installing-an-eap-method"></a>Instalando um método EAP

Siga as instruções abaixo para instalar um método EAP implementado pelo usuário em um computador cliente que executa o EAPHost.

-   Implemente [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DLLUNREGISTERSERVER**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) para a DLL do método EAP. Essas funções adicionam e removem as chaves do registro apropriadas para o método EAP durante o processo de instalação e (desinstalação).

    Para obter informações sobre as chaves de registro específicas associadas à instalação de um método EAP, consulte o tópico [configuração do registro para métodos EAP](registry-keys-for-eap-methods.md) .

-   Instale a DLL que contém a implementação do método EAP com o comando do console a seguir.

     *&lt; Nome &gt; da dll* regsvr32.exe

    Para desinstalar a DLL, use o seguinte comando de console:

    **regsvr32.exe** **/u** *&lt; nome &gt; da dll*

-   Reinicie o serviço EAPHost.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o EAPHost](using-eap-host.md)
</dt> </dl>

 

 
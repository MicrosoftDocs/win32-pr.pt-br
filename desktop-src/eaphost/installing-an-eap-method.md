---
title: Instalando um método EAP
description: Siga as instruções abaixo para instalar um método EAP implementado pelo usuário em um computador cliente que executa o EAPHost.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e047c5a8f0bc4cedcc207016d6f66530b392869839dda128635cd31ac459011a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021576"
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

 

 
---
description: Um número limitado de objetos de dados privados está disponível em cada sistema com a finalidade de armazenar informações de maneira protegida e criptografada.
ms.assetid: 927473d7-b5bc-4b6f-b303-8a0f8680731d
title: Objeto de dados particulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccacd1334c9859495acf89075b77a0f10af4cb64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090185"
---
# <a name="private-data-object"></a>Objeto de dados particulares

Um número limitado de objetos de dados privados está disponível em cada sistema com a finalidade de armazenar informações de maneira protegida e criptografada.

Os objetos de dados privados são fornecidos principalmente para dar suporte ao armazenamento de senhas de conta de servidor. Isso é útil para servidores que são executados em uma conta específica. A senha da conta do servidor é de dados privados que devem ser protegidos, mas é necessário para fazer logon no servidor.

Os objetos de dados privados podem ser de uso geral ou podem ser um dos três tipos especializados: local, global e computador.

Os objetos de dados privados locais só podem ser lidos localmente do computador que armazena o objeto. A tentativa de lê-los remotamente resulta em um \_ erro de acesso \_ negado ao status. Os objetos de dados privados locais têm nomes de chave que começam com o prefixo "L $". Além dos objetos privados locais que você cria, o sistema operacional define os seguintes objetos privados locais: $machine. ACC, SAC, SAI e SANSC.

Os objetos de dados privados globais são globais no sentido de que, se forem criados em um controlador de domínio, eles serão replicados automaticamente para todos os controladores de domínio nesse domínio. Em outras palavras, cada controlador de domínio nesse domínio terá acesso aos valores que o objeto de dados privados global contém. Por outro lado, os objetos de dados privados globais criados em um sistema que não é um controlador de domínio, bem como objetos de dados privados não globais, não são replicados. Os objetos de dados privados globais têm nomes de chave que começam com "G $".

Os objetos de dados privados do computador podem ser acessados somente pelo sistema operacional. Esses objetos têm nomes de chave que começam com "M $".

**Observação**  Você pode definir, mas não pode recuperar, objetos de dados privados do computador.

Além desses prefixos, os valores a seguir também indicam os objetos locais ou de máquina. Esses valores têm suporte para compatibilidade com versões anteriores e não devem ser usados quando você cria novos objetos locais ou de máquina. O nome da chave dos objetos de dados privados locais também pode começar com "RasDialParms" ou "RasCredentials". O nome da chave para objetos de computador também pode começar com, "NL $" ou " \_ sc \_ ".

Objetos de dados privados que não são um dos tipos especializados anteriores usam nomes de chave que não começam com um prefixo. Esses objetos não são replicados e podem ser lidos localmente ou remotamente por aplicativos.

 

 




---
title: Criando scripts de objetos COM em aplicativos personalizados
description: Criando scripts de objetos COM em aplicativos personalizados
ms.assetid: 14e8cd53-e2b2-4393-8961-32efdf269f76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d16938747755dfb0c08907430837de5a1106ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159702"
---
# <a name="scripting-com-objects-in-custom-applications"></a>Criando scripts de objetos COM em aplicativos personalizados

A Microsoft fornece vários ambientes para criar scripts de objetos COM: Active Server páginas, Windows Script Host e assim por diante. ISVs (fornecedores independentes de software) também podem licenciar os mecanismos de script da Microsoft para uso em seus aplicativos. Por exemplo, um ISV que cria um processador de texto pode querer adicionar uma linguagem de macro ao aplicativo para que os usuários pudessem automatizar tarefas simples. Ao licenciar um mecanismo de script, o ISV pode usar uma linguagem como VBScript ou JScript como linguagem de macro do aplicativo.

Além de licenciar os mecanismos de script VBScript e JScript, os ISVs podem gravar seus próprios mecanismos de script do ActiveX. Esses mecanismos de script podem então ser conectados a qualquer ambiente de host que dê suporte ao padrão do mecanismo de script do ActiveX. Por exemplo, um ISV pode escrever um mecanismo de script PerlScript e instalá-lo em um servidor ASP, permitindo assim que o servidor ASP processe scripts PerlScript.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando scripts com objetos COM](scripting-with-com-objects.md)
</dt> </dl>

 

 





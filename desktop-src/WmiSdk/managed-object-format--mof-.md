---
description: Formato MOF (MOF) é a linguagem usada para descrever as classes de modelo CIM (CIM).
ms.assetid: 26494142-2078-4d46-a794-e43973255c2d
ms.tgt_platform: multiple
title: MOF (Managed Object Format)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16f95c6868943a2f41c4326c341207ff26a03af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763214"
---
# <a name="managed-object-format-mof"></a>MOF (Managed Object Format)

Formato MOF (MOF) é a linguagem usada para descrever as classes [*de modelo CIM (CIM)*](gloss-c.md) .

A maneira recomendada para os provedores WMI implementarem novas classes WMI é em arquivos MOF que são compilados usando [**Mofcomp.exe**](mofcomp.md) no [*repositório WMI*](gloss-w.md). Também é possível criar e manipular classes e instâncias CIM usando a [API com para o WMI](com-api-for-wmi.md).

Um provedor WMI normalmente consiste em um arquivo MOF, que define os dados e as classes de evento para os quais o provedor retorna dados e um arquivo DLL que contém o código que fornece dados. Para obter mais informações, consulte [fornecendo dados ao WMI](providing-data-to-wmi.md).

Os aplicativos e scripts do cliente WMI podem consultar instâncias de classes do provedor MOF ou assinar para receber notificações de eventos.

Você pode executar as seguintes tarefas com o MOF:

-   [Compilando arquivos MOF](compiling-mof-files.md)
-   [Criando uma classe](creating-a-class.md)
-   [Criando uma instância](creating-an-instance.md)
-   [Criando um método](creating-a-method.md)
-   [Adicionando um qualificador](adding-a-qualifier.md)
-   [Criando um comentário](creating-a-comment.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o WMI](about-wmi.md)
</dt> </dl>

 

 




---
description: Criando o arquivo de recurso de idioma base
ms.assetid: 770e1f4b-5258-4b6b-afa4-5c19743daaaa
title: Criando o arquivo de recurso de idioma base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96d566625025c105e123e0e2edf9f4f20721274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011634"
---
# <a name="creating-the-base-language-resource-file"></a>Criando o arquivo de recurso de idioma base

Os recursos dos elementos da interface do usuário são definidos para a linguagem básica à qual o aplicativo dá suporte, por exemplo, inglês (Estados Unidos). Um exemplo de um arquivo de recurso do Win32 PE é um arquivo. rc, criado usando o compilador RC. Para obter detalhes sobre a criação do arquivo. rc, consulte [sobre os arquivos de recurso](../menurc/about-resource-files.md).

Se estiver usando um arquivo. rc para os recursos de idioma base, você terá a opção de usar um arquivo de configuração de recurso para uma representação XML dos dados de configuração de recursos. Para criar esse arquivo, consulte [preparando um arquivo de configuração de recurso](preparing-a-resource-configuration-file.md).

Você também pode usar um arquivo PE não Win32 para definir recursos de idioma base. Por exemplo, você pode usar um arquivo. xml ou. txt para essa finalidade.

> [!Note]  
> Ao definir recursos de idioma base usando um arquivo PE não Win32, você não pode usar o compilador RC para definição de recurso. Em vez disso, você define seu próprio formato de recurso e seu aplicativo deve fornecer sua própria funcionalidade para localizar e carregar os recursos necessários.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Preparando recursos](preparing-resources.md)
</dt> <dt>

[Preparando um arquivo de configuração de recurso](preparing-a-resource-configuration-file.md)
</dt> </dl>

 

 

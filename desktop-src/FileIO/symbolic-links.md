---
description: Um link simbólico é um objeto do sistema de arquivos que aponta para outro objeto do sistema de arquivos. O objeto que está sendo apontado é chamado de destino.
ms.assetid: d6bf5df7-bc12-4dec-b116-95d9109f5eb4
title: Links simbólicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 126897dc230b36f504ef17653daea32b1076d10870a3a22015462f3abec05448
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951025"
---
# <a name="symbolic-links"></a>Links simbólicos

Um link simbólico é um objeto do sistema de arquivos que aponta para outro objeto do sistema de arquivos. O objeto que está sendo apontado é chamado de destino.

Links simbólicos são transparentes para os usuários; os links aparecem como arquivos ou diretórios normais e podem ser afetados pelo usuário ou aplicativo exatamente da mesma maneira.

links simbólicos são projetados para auxiliar na migração e na compatibilidade de aplicativos com UNIX sistemas operacionais. a Microsoft implementou seus links simbólicos para funcionar exatamente como UNIX links.

Para obter mais informações, consulte estes tópicos.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                             | Descrição                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Efeitos de link simbólico em funções de sistemas de arquivos](symbolic-link-effects-on-file-systems-functions.md)<br/> | Como os links simbólicos afetam as funções de arquivo padrão que usam nomes de caminho para especificar um ou mais arquivos.<br/>                                        |
| [Considerações sobre programação](symbolic-link-programming-considerations.md)<br/>                             | Considerações sobre programação para trabalhar com links simbólicos.<br/>                                                                                |
| [Criando links simbólicos](creating-symbolic-links.md)<br/>                                                 | Crie links simbólicos que usam um caminho absoluto ou relativo usando a função [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) .<br/> |



 

## <a name="supported-operating-systems"></a>Sistemas operacionais com suporte

links simbólicos estão disponíveis em NTFS a partir do Windows Vista.

 

 





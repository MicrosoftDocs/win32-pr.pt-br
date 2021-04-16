---
description: Comece a criar o pacote de atualização copiando o pacote de instalação e a árvore de diretórios de origem do produto original.
ms.assetid: 279f0ab6-a6fc-4594-af6c-5a69d6167300
title: Importando banco de dados de instalação original
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390a51e1ef068124fcdf85142ab01406d92f9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750237"
---
# <a name="importing-original-installation-database"></a>Importando banco de dados de instalação original

Comece a criar o pacote de atualização copiando o pacote de instalação e a árvore de diretórios de origem do produto original. As instruções para criar o pacote de instalação para MNP2000 são fornecidas em [um exemplo de instalação](an-installation-example.md). Você deve copiar o conteúdo das seguintes pastas:

C: \\MNP2000.msi de exemplo \\

C: \\ bloco de notas de exemplo \\\\

C: \\ exemplo de \\ binário\\

C: \\ ícone de exemplo \\\\

Atualize o conteúdo da pasta do bloco de notas para que corresponda à fonte descrita em [planejando uma atualização principal](planning-a-major-upgrade.md). Remova todos os arquivos de origem obsoletos, como Baseball.txt, e substitua pelos arquivos atualizados, como Baseba01.txt. Adicione os novos arquivos adicionais fornecidos pela atualização, como Opera01.txt.

Renomear MNP2000.msi para MNP2001.msi. Nas etapas subsequentes, você usará um editor de tabela para modificar esse banco de dados no arquivo. msi para a atualização. As tabelas de banco de dados que não são explicitamente modificadas nas seções subsequentes são idênticas às tabelas no banco de dados do produto original, MNP2000.msi.

[Continuar](updating-directory-structure-for-an-upgrade.md)

 

 




---
description: Windows Installer instala e remove um aplicativo ou produto em partes referenciadas como componentes.
ms.assetid: 949d8b8c-8f1a-4fde-9a7d-824d33436e62
title: Organizando aplicativos em componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3fc2db794bef2a29025bf7ebc54c65691145ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828028"
---
# <a name="organizing-applications-into-components"></a>Organizando aplicativos em componentes

Windows Installer instala e remove um aplicativo ou produto em partes referenciadas como [componentes](windows-installer-components.md). Os componentes são coleções de recursos que são sempre instalados ou removidos como uma unidade do sistema de um usuário. Um recurso pode ser um arquivo, chave do registro, atalho ou qualquer outra coisa que possa ser instalada. Cada componente recebe um [GUID](guid.md)de código de componente exclusivo.

Os autores de pacotes de instalação devem criar apenas componentes e versões de componentes, que podem ser instalados e removidos sem danificar outros componentes. Além disso, a remoção de um componente não deve deixar por trás de nenhum recurso órfão no computador do usuário, como arquivos não utilizados, chaves do registro ou atalhos. Para garantir isso, os autores devem aderir às seguintes regras gerais ao organizar recursos em componentes:

-   Nunca crie dois componentes que instalem um recurso sob o mesmo nome e local de destino. Se um recurso precisar ser duplicado em vários componentes, altere seu nome ou local de destino em cada componente. Essa regra deve ser aplicada em aplicativos, produtos, versões do produto e empresas.
-   Observe que a regra anterior significa que dois componentes não devem ter o mesmo arquivo de caminho de chave. O valor de caminho de chave aponta para um arquivo ou pasta em particular que pertence ao componente que o instalador usa para detectar o componente. Se dois componentes tivessem o mesmo arquivo de caminho de chave, o instalador não conseguiria distinguir qual componente está instalado. No entanto, dois componentes podem compartilhar uma pasta de caminho de chave.
-   Não crie uma versão de um componente que seja incompatível com todas as versões anteriores do componente. O componente pode ser compartilhado por outros aplicativos, produtos, versões de produtos e empresas. Em vez disso, crie um novo componente.
-   Não crie componentes que contenham recursos que deverão ser instalados em mais de um diretório no sistema do usuário. O instalador instala todos os recursos em um componente no mesmo diretório. Não é possível instalar alguns recursos em subdiretórios.
-   Não inclua mais de um servidor COM por componente. Se um componente contiver um servidor COM, ele deverá ser o caminho de chave para o componente.
-   Não especifique mais de um arquivo por componente como um destino para o menu **Iniciar** ou um atalho da área de trabalho.

Ao organizar um aplicativo em componentes, os autores de pacotes podem precisar adicionar, remover ou modificar os recursos em uma instalação existente. Nesse caso, o autor deve decidir se deseja fornecer os recursos introduzindo um novo componente ou modificando componentes existentes e alterando-os para uma nova versão do componente. Como um código de componente exclusivo deve ser atribuído quando um novo componente é introduzido, os autores devem determinar se suas alterações exigem a alteração do código do componente. Para obter mais informações, consulte [alterando o código do componente](changing-the-component-code.md), [o que acontecerá se as regras de componente forem interrompidas?](what-happens-if-the-component-rules-are-broken.md)e [definir os componentes do instalador](defining-installer-components.md).

 

 




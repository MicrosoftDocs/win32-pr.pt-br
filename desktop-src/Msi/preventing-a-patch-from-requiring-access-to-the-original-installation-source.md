---
description: Não é possível eliminar todas as circunstâncias sob as quais a aplicação de um patch pode exigir acesso à fonte de instalação original.
ms.assetid: f7028c55-e4a5-4596-af7a-728c9f4f367e
title: Impedir que um patch exija acesso à fonte de instalação original
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baee8b261ff0a3f6bb94fb141ee765726ffa2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828023"
---
# <a name="preventing-a-patch-from-requiring-access-to-the-original-installation-source"></a>Impedir que um patch exija acesso à fonte de instalação original

Não é possível eliminar todas as circunstâncias sob as quais a aplicação de um patch pode exigir acesso à fonte de instalação original.

Siga os seguintes pontos para minimizar a possibilidade de que seu patch exija acesso à fonte original:

-   Usar patches de arquivo inteiro somente. Isso elimina a necessidade de criar patches binários para todas as versões lançadas anteriormente do arquivo. Observe que os patches de arquivo inteiros são geralmente maiores em tamanho que os patches binários. Você pode definir facilmente um patch para ser um patch de arquivo inteiro, criando a propriedade IncludeWholeFilesOnly com um valor de 1 (um) no arquivo PCP (Propriedades de criação de patch).
-   Certifique-se de que nenhuma das suas ações personalizadas acesse o local de origem original.
-   Certifique-se de que a ação resolver seja condicional para que seja executada apenas quando necessário, ou, como alternativa, não esteja presente.
-   Preencha a [tabela MsiFileHash](msifilehash-table.md) para todos os arquivos com versão não versionada. A ferramenta SDK do Windows Installer, Msifiler.exe, pode facilmente fazer isso para você.
-   Verifique se todos os arquivos têm a versão e as informações de idioma corretas. A ferramenta SDK do Windows Installer, Msifiler.exe, pode facilmente fazer isso para você.

## <a name="source-requirements-when-patching"></a>Requisitos de origem ao aplicar patches

O acesso às fontes de instalação originais pode ser necessário para aplicar o patch nos seguintes casos:

-   O patch se aplica a um recurso que é executado no momento da origem. Nesse caso, o recurso é transferido do estado de execução da origem para o estado local.
-   O patch se aplica a um componente que tem um arquivo ausente ou corrompido.
-   O patch se aplica a um arquivo em um componente que também contém arquivos sem versão sem entradas MsiFileHash. Uma [tabela MsiFileHash](msifilehash-table.md) populada é necessária para impedir a recópia desnecessária de arquivos não versionáveis do local de origem.
-   O patch foi aplicado com uma reinstalaçãomode de amus ou emus. Essa opção é perigosa, pois executa operações de cópia de arquivo independentemente da versão do arquivo. Isso pode levar a reving de arquivos e quase sempre requer a origem. O valor recomendado de reinstalaçãomode é omus.
-   O pacote armazenado em cache para o produto está ausente. O pacote armazenado em cache é necessário para a aplicação de um patch. O pacote armazenado em cache é armazenado na pasta% windir% \\ Installer.
-   O pacote é criado para fazer uma chamada para a [ação resolver](resolvesource-action.md). Essa ação deve, em geral, ser evitada ou condicionalmente apropriada, porque sua execução sempre resulta em um acesso à origem.
-   O pacote tem uma ação personalizada que tenta acessar a fonte de alguma maneira. O exemplo mais comum é uma ação personalizada de tipo 23 de instalação simultânea.
    > [!Note]  
    > As instalações simultâneas não são recomendadas para a instalação de aplicativos destinados ao lançamento para o público. Para obter informações sobre instalações simultâneas, consulte [instalações simultâneas](concurrent-installations.md).

     

-   O pacote de patch consiste em patches binários que não se aplicam à versão atual do arquivo no computador.

Considere o exemplo a seguir em que Windows Installer requer acesso à fonte original ao aplicar um patch:

1.  Instale a versão RTM do exemplo de produto.
2.  Aplique o patch Qfe1. msp ao computador. Esta versão de patches 1,0 do Example.dll para a versão 1,1.
3.  Um novo patch, Qfe2. msp, é fornecido, que atualiza Example.dll para a versão 1,2 e os obsoletos Qfe1. msp. No entanto, o patch foi criado apenas para a versão de destino 1,0 do Example.dll porque ele foi gerado usando a versão RTM do produto. A versão 1,2 do Example.dll inclui a correção contida na versão 1,1 do Example.dll, mas o arquivo. msp foi gerado entre as imagens RTM e QFE2. Assim, quando o Qfe2. msp é aplicado ao computador, Windows Installer precisa acessar a fonte original. O patch binário do Example.dll não pode ser aplicado à versão 1,1; Ele só pode ser aplicado à versão 1,0. Isso faz com que o instalador recopie a versão 1,0 de Example.dll do local de origem original para que o patch possa ser aplicado com êxito.

## <a name="source-requirements-when-removing-a-patch"></a>Requisitos de origem ao remover um patch

O acesso às fontes de instalação originais pode ser necessário para remover um patch se o Windows Installer não armazenou informações de linha de base sobre o patch. A partir do Windows Installer 3,0, o instalador salva seletivamente as informações de linha de base sobre os arquivos quando eles são atualizados. Para obter mais informações sobre o cache de linha de base, consulte [reduzindo o tamanho do patch](reducing-patch-size.md) .

 

 




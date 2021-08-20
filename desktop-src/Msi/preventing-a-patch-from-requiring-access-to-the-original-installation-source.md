---
description: Não é possível eliminar todas as circunstâncias nas quais a aplicação de um patch pode exigir acesso à fonte de instalação original.
ms.assetid: f7028c55-e4a5-4596-af7a-728c9f4f367e
title: Impedindo que um patch exija acesso à origem da instalação original
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5dcadae12b733d76dee8c3acd5ec6af6169c47cfd8c7eeb22ad9693a75859a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376785"
---
# <a name="preventing-a-patch-from-requiring-access-to-the-original-installation-source"></a>Impedindo que um patch exija acesso à origem da instalação original

Não é possível eliminar todas as circunstâncias nas quais a aplicação de um patch pode exigir acesso à fonte de instalação original.

Adera aos seguintes pontos para minimizar a possibilidade de que o patch exigirá acesso à origem original:

-   Use patches somente de arquivo inteiro. Isso elimina a necessidade de criar patches binários para todas as versões lançadas anteriormente do arquivo. Observe que os patches de arquivo inteiros geralmente são maiores do que patches binários. Você pode definir facilmente um patch para ser um patch de arquivo inteiro com a criação da propriedade IncludeWholeFilesOnly com um valor de 1 (um) no arquivo PCP (Propriedades de Criação de Patch).
-   Certifique-se de que nenhuma de suas ações personalizadas acesse o local de origem original.
-   Verifique se a ação ResolveSource está condicionalizada para que ela seja executado somente quando necessário ou, como alternativa, não está presente.
-   Preencha a Tabela [MsiFileHash para](msifilehash-table.md) todos os arquivos sem versão. A Windows SDK do Instalador do Msifiler.exe, pode fazer isso facilmente para você.
-   Verifique se todos os arquivos têm a versão e as informações de idioma corretas. A Windows SDK do Instalador do Msifiler.exe, pode fazer isso facilmente para você.

## <a name="source-requirements-when-patching"></a>Requisitos de origem ao fazer patch

O acesso às fontes de instalação originais pode ser necessário para aplicar o patch nos seguintes casos:

-   O patch se aplica a um recurso que atualmente é executado da origem. Nesse caso, o recurso é transigido do estado de run-from-source para o estado local.
-   O patch se aplica a um componente que tem um arquivo ausente ou corrompido.
-   O patch se aplica a um arquivo em um componente que também contém arquivos sem versão sem entradas MsiFileHash. Uma tabela [MsiFileHash](msifilehash-table.md) populada é necessária para evitar a cópia desnecessária de arquivos sem versão do local de origem.
-   O patch foi aplicado com um REINSTALLMODE de amus ou emus. Essa opção é perigosa porque executa operações de cópia de arquivo, independentemente da versão do arquivo. Isso pode levar à re rotação de arquivos e quase sempre requer a origem. O valor reINSTALLMODE recomendado é omus.
-   O pacote armazenado em cache para o produto está ausente. O pacote armazenado em cache é necessário para a aplicação de um patch. O pacote armazenado em cache é armazenado na pasta %windir% \\ installer.
-   O pacote é autor para fazer uma chamada para a [ação ResolveSource](resolvesource-action.md). Essa ação geralmente deve ser evitada ou condicionada adequadamente, pois sua execução sempre resulta em um acesso à origem.
-   O pacote tem uma ação personalizada que tenta acessar a origem de alguma maneira. O exemplo mais comum é uma ação personalizada de instalação simultânea do tipo 23.
    > [!Note]  
    > Instalações simultâneas não são recomendadas para a instalação de aplicativos destinados à versão para o público. Para obter informações sobre instalações simultâneas, consulte [Instalações simultâneas.](concurrent-installations.md)

     

-   O pacote de patch consiste em patches binários que não se aplicam à versão atual do arquivo no computador.

Considere o exemplo a seguir em que Windows Instalador requer acesso à origem original ao aplicar um patch:

1.  Instale a versão RTM do exemplo do produto.
2.  Aplique o patch Qfe1.msp ao computador. Isso remenda a versão 1.0 do Example.dll para a versão 1.1.
3.  Um novo patch, Qfe2.msp, é fornecido, que atualiza o Example.dll para a versão 1.2 e o Qfe1.msp obsoleto. No entanto, o patch só foi criado para ser destinado à versão 1.0 do Example.dll porque ele foi gerado usando a versão RTM do produto. Example.dll versão 1.2 inclui a correção contida no Example.dll versão 1.1, mas o arquivo .msp foi gerado entre as imagens RTM e QFE2. Portanto, quando qfe2.msp é aplicado ao computador, Windows Instalador precisa acessar a origem original. O patch binário para Example.dll não pode ser aplicado à versão 1.1; ele só pode se aplicar à versão 1.0. Isso resulta na cópia do Instalador versão 1.0 do Example.dll do local de origem original para que o patch possa ser aplicado com êxito.

## <a name="source-requirements-when-removing-a-patch"></a>Requisitos de origem ao remover um patch

O acesso às fontes de instalação originais poderá ser necessário para remover um patch se o instalador do Windows não tiver armazenado informações de linha de base sobre o patch. A partir do Windows 3.0, o instalador salva seletivamente informações de linha de base sobre arquivos quando eles são atualizados. Para obter mais informações sobre o cache de linha de base, consulte [Reduzindo o tamanho do patch.](reducing-patch-size.md)

 

 




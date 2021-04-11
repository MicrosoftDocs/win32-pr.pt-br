---
title: Atualizando licenças para lojas que têm o logotipo do PlaysForSure
description: Atualizando licenças para lojas que têm o logotipo do PlaysForSure
ms.assetid: d08d6b6e-937e-4dec-b7ca-376cdad069f9
keywords:
- Armazenamentos online do Windows Media Player, atualizando licenças
- lojas online, atualização de licenças
- Lojas online do Windows Media Player, atualizando licenças
- lojas online, atualizando licenças
- Lojas online do Windows Media Player, logotipo do PlaysForSure
- lojas online, logotipo do PlaysForSure
- Atualizando licenças
- licenças, atualizando
- PlaysForSure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e48a3ddfd2b0670e3720f7c71587d0330a69a7
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104084368"
---
# <a name="refreshing-licenses-for-stores-that-have-the-playsforsure-logo"></a>Atualizando licenças para lojas que têm o logotipo do PlaysForSure

Algumas lojas de música online têm o logotipo do PlaysForSure, mas não estão integradas ao Windows Media Player 11. Esses armazenamentos devem fornecer um documento de informações e um componente leve para que o Windows Media Player 11 possa obter e atualizar licenças para seu conteúdo.

O exemplo a seguir ilustra como o processo de atualização de licença funciona.

1.  O usuário obtém faixas de música de 50 da loja online da Proseware. Cada faixa é um arquivo com a extensão de nome de arquivo. WMA. Juntamente com as faixas, o usuário obtém licenças para reproduzir as faixas.
2.  O usuário copia as faixas 50 para um novo computador que tem o Windows Media Player 11 instalado e adiciona as faixas à biblioteca do Windows Media Player.
3.  Em algum momento posterior, o módulo de atualização de licença (LRM), que faz parte do Windows Media Player 11, inspeciona os metadados nas faixas 50 e determina que o Proseware é o provedor de conteúdo.
    > [!Note]  
    > O Windows Media Player é capaz de identificar o provedor de conteúdo inspecionando o atributo **ContentDistributor** em um arquivo de mídia. Se uma loja online que tem o logotipo do PlaysForSure fornecer um arquivo de mídia que usa o Windows Media Digital Rights Management (WMDRM), o repositório online deverá posicionar o atributo **ContentDistributor** no arquivo de mídia. Para obter mais informações, consulte Adicionando o atributo de distribuidor de conteúdo no SDK do Windows Media Player.

     

4.  O LRM pesquisa a URL do documento de informações da Proseware, baixa o documento e inspeciona o elemento de **instalação** do documento para obter a URL de um pacote que o LRM pode usar para instalar o componente da Proseware. O LRM instala e carrega o componente.
5.  Para cada uma das faixas 50, o LRM chama o método [IWMPSubscriptionService:: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) do componente da Proseware. O método **allowPlay** coloca uma licença para a faixa individual no novo computador e retorna **true** no parâmetro *pfAllowPlay* .
    > [!Note]  
    > O componente Proseware deve fornecer todas as licenças necessárias para reproduzir a faixa individual. Ou seja, o componente deve fornecer uma licença raiz e uma folha, se necessário.

     

    Durante a primeira chamada para o método **allowPlay** , o componente Proseware deve exibir uma caixa de diálogo para verificar se o usuário atual tem uma conta de Proseware e tem o direito de reproduzir o controle. Durante as chamadas subsequentes para **allowPlay**, o componente pode usar as credenciais que ele obteve na primeira chamada para verificar se o usuário tem o direito de reproduzir as faixas restantes.

O componente, que é gravado pela loja online, deve implementar o método **allowPlay** da interface **IWMPSubscriptionService** . O componente deve retornar E \_ NOTIMPL de cada um dos três métodos: **allowCDBurn**, **allowPDATransfer** e **startBackgroundProcessing**. Além disso, o componente deve definir o valor da entrada de registro **Capabilities** como 1; ou seja, o \_ sinalizador de recurso ALLOWPLAY de limite de assinatura \_ deve ser definido e todos os outros sinalizadores de funcionalidade devem ser limpos. Para obter mais informações sobre como registrar o componente, consulte [chaves e entradas do registro para uma loja online tipo 2](registry-keys-and-entries-for-a-type-2-online-store.md).

Para obter informações sobre como criar um componente que implementa a interface **IWMPSubscriptionService** , consulte [criando o plug-in para uma loja online tipo 2](building-the-plug-in-for-a-type-2-online-store.md).

Para obter informações sobre como fornecer um documento de informações da Microsoft, envie um email para a equipe de serviços virtuais do Windows Media Player. O endereço de email da equipe é mpsvctm@microsoft.com .

Para obter orientações técnicas sobre como usar uma variedade de SDKs do Windows Media para criar um serviço que oferece conteúdo de mídia digital licenciado, vá para o [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx) e procure "criando uma assinatura online do Windows Media Player 10".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Documento do serviceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Lojas online do Windows Media Player**](windows-media-player-online-stores.md)
</dt> </dl>

 

 





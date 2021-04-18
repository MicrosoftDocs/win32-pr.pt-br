---
title: Instalando de um CD enquanto estiver online
description: Instalando de um CD enquanto estiver online
ms.assetid: 4cf34f0e-caa0-42d1-b99a-51bbb7f0a7df
keywords:
- Armazenamentos online do Windows Media Player, instalando do CD enquanto estiver online
- lojas online, instalando do CD enquanto estiver online
- Digite 1 lojas online, instalando do CD enquanto estiver online
- Digite 2 lojas online, instalando do CD enquanto estiver online
- Armazenamentos online do Windows Media Player, instalações online do CD
- lojas online, instalações online do CD
- Digite 1 lojas online, instalações online do CD
- Digite 2 lojas online, instalações online do CD
- Armazenamentos online do Windows Media Player, instalações de CD quando estiverem online
- lojas online, instalações de CD enquanto estão online
- Digite 1 lojas online, instalações de CD quando estiverem online
- Digite 2 lojas online, instalações de CD quando estiverem online
- Instalando lojas online do CD enquanto estiver online
- Instalações de CD de lojas online enquanto estão online
- instalações online de lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd57015e64dece444b1a91afebe3144bee117caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105800127"
---
# <a name="installing-from-a-cd-while-online"></a>Instalando de um CD enquanto estiver online

Os usuários podem instalar o Windows Media Player a partir de um CD enquanto estiverem conectados à Internet. Quando isso acontece, a instalação do Windows Media Player localiza o documento serviceInfo especificado pelo parâmetro de linha de comando *serviceInfo* . Se o atributo de **chave** corresponder ao parâmetro de linha de comando *defaultservice* , a instalação inspecionará o elemento install para personalizar o processo de instalação. Usando os valores de atributo, a instalação exibe o contrato de licença de usuário final (EULA) e sua declaração de privacidade, além de recuperar e instalar o arquivo. cab no computador do usuário. Por exemplo, você pode usar esse recurso para instalar a versão mais recente de um objeto COM que sua loja online requer.

Após a instalação, o Windows Media Player define o armazenamento online inicial usando o nome da chave que você especificou para o parâmetro de linha de comando *defaultservice* .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento de instalação**](install-element.md)
</dt> <dt>

[**Documento do serviceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Configurando a loja online inicial**](setting-the-initial-online-store.md)
</dt> <dt>

[**Parâmetros de linha de comando de instalação para lojas online**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 





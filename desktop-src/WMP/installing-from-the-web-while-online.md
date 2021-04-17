---
title: Instalando a partir da Web enquanto estiver online
description: Instalando a partir da Web enquanto estiver online
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Armazenamentos online do Windows Media Player, instalando da Web enquanto estiver online
- lojas online, instalando da Web enquanto estiver online
- Digite 1 lojas online, instalando da Web enquanto estiver online
- Digite 2 lojas online, instalando da Web enquanto estiver online
- Lojas online do Windows Media Player, instalações online da Web
- lojas online, instalações online da Web
- Digite 1 lojas online, instalações online da Web
- Digite 2 lojas online, instalações online da Web
- Instalando lojas online da Web enquanto estiver online
- instalações online de lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd342d3fc79cf3012d5bc290561a9b63167e044f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105770487"
---
# <a name="installing-from-the-web-while-online"></a>Instalando a partir da Web enquanto estiver online

Os usuários podem instalar o Windows Media Player como um download da Web enquanto estiver conectado à Internet. Nesse caso, a Microsoft pode configurar a loja online inicial que você especificar.

Para redistribuir o Windows Media Player dessa maneira, use a seguinte URL:

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*versão*&userlocalize =*LocalId*&Service =*Key*

Na URL anterior, defina *chave* como o nome da chave para sua loja online e defina *LocaleID* como o identificador da localidade onde sua loja fornece o serviço. Defina a *versão* como 2 para Windows Media Player 11 no Windows XP ou 1 para Windows Media Player 10. A URL instala o Windows Media Player e define o repositório ativo inicial para aquele especificado por *chave*.

O exemplo a seguir mostra uma URL que instala o Windows Media Player 11 e define o Proseware como o repositório ativo inicial. O valor de 409 para *LocaleID* indica que o Proseware fornece serviço no Estados Unidos.

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

Se o documento do serviceInfo para a loja online incluir um elemento de instalação, a instalação do Windows Media Player personalizará o processo de instalação. Usando os valores de atributo, a instalação exibe o contrato de licença de usuário final (EULA) e sua declaração de privacidade, além de recuperar e instalar o arquivo. cab no computador do usuário. Por exemplo, você pode usar esse recurso para instalar a versão mais recente de um objeto COM que sua loja online requer.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento de instalação**](install-element.md)
</dt> <dt>

[**Documento do serviceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Configurando a loja online inicial**](setting-the-initial-online-store.md)
</dt> </dl>

 

 





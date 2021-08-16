---
title: Instalando a partir da Web enquanto estiver online
description: Instalando a partir da Web enquanto estiver online
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Windows Media Player lojas online, instalando da Web enquanto estiver online
- lojas online, instalando da Web enquanto estiver online
- Digite 1 lojas online, instalando da Web enquanto estiver online
- Digite 2 lojas online, instalando da Web enquanto estiver online
- Windows Media Player lojas online, instalações online da Web
- lojas online, instalações online da Web
- Digite 1 lojas online, instalações online da Web
- Digite 2 lojas online, instalações online da Web
- Instalando lojas online da Web enquanto estiver online
- instalações online de lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801dd9fbee8bff2660a39f6b40e8a5a9e703df00f82be54a7b93c0d200d2ccea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135549"
---
# <a name="installing-from-the-web-while-online"></a>Instalando a partir da Web enquanto estiver online

os usuários podem instalar Windows Media Player como um download da Web enquanto estiverem conectados à Internet. Nesse caso, a Microsoft pode configurar a loja online inicial que você especificar.

para redistribuir Windows Media Player dessa maneira, use a seguinte URL:

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*versão*&userlocalize =*LocalId*&Service =*Key*

Na URL anterior, defina *chave* como o nome da chave para sua loja online e defina *LocaleID* como o identificador da localidade onde sua loja fornece o serviço. defina a *versão* como 2 para Windows Media Player 11 no Windows XP ou 1 para Windows Media Player 10. a URL instala Windows Media Player e define o repositório ativo inicial como o especificado por *chave*.

o exemplo a seguir mostra uma URL que instala o Windows Media Player 11 e define o proseware como o repositório ativo inicial. O valor de 409 para *LocaleID* indica que o Proseware fornece serviço no Estados Unidos.

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

se o documento do serviceinfo para a loja online incluir um elemento de instalação, Windows Media Player a instalação personalizará o processo de instalação. Usando os valores de atributo, a instalação exibe o EULA (contrato de licença de usuário final) e sua declaração de privacidade, além de recuperar e instalar o arquivo de .cab no computador do usuário. Por exemplo, você pode usar esse recurso para instalar a versão mais recente de um objeto COM que sua loja online requer.

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

 

 





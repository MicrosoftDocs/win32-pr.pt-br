---
title: Parâmetros de linha de comando de instalação para lojas online
description: Parâmetros de linha de comando de instalação para lojas online
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Armazenamentos online do Windows Media Player, parâmetros de linha de comando de instalação
- lojas online, parâmetros de linha de comando de instalação
- Digite 1 lojas online, parâmetros de linha de comando de instalação
- Digite 2 lojas online, parâmetros de linha de comando de instalação
- parâmetros de linha de comando da instalação
- Lojas online do Windows Media Player, parâmetros de linha de comando
- lojas online, parâmetros de linha de comando
- tipo 1 lojas online, parâmetros de linha de comando
- tipo 2 lojas online, parâmetros de linha de comando
- parâmetros de linha de comando
- Armazenamentos online do Windows Media Player, parâmetros
- lojas online, parâmetros
- tipo 1 lojas online, parâmetros
- tipo 2 lojas online, parâmetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0605814d3f8ce5e3015cf67d38f213a6b6f07500
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005451"
---
# <a name="setup-command-line-parameters-for-online-stores"></a>Parâmetros de linha de comando de instalação para lojas online

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

Ao instalar o Windows Media Player 10 ou o Windows Media Player 11 no Windows XP, você pode acrescentar parâmetros de linha de comando para especificar a primeira loja online que o usuário vê.

Sintaxe


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:serviceKey /ServiceInfo:documentPath /ServiceExtra:queryString"
```



Parâmetros

Defaultservice (obrigatório)

O nome da chave para a loja online. Esse valor deve corresponder ao nome da chave no atributo de **chave** do elemento **serviceInfo** do documento serviceInfo.

ServiceInfo (obrigatório)

O caminho totalmente qualificado para um documento do serviceInfo instalado no computador do usuário.

Userextra (opcional)

Uma cadeia de caracteres de consulta que o Windows Media Player 10 acrescentará à URL do documento do serviceInfo quando recuperar o documento online.

## <a name="remarks"></a>Comentários

Para obter detalhes sobre como redistribuir o software do Windows Media Player com seu aplicativo, consulte [redistribuindo o software do Windows Media Player](redistributing-windows-media-player-software.md).

Quando o computador do usuário não está conectado à Internet, as informações contidas no documento local de informações são usadas para configurar o Windows Media Player para o serviço ativo inicial.

Os parâmetros de linha de comando diferenciam maiúsculas de minúsculas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lojas online de co-identidade visual**](co-branding-online-stores.md)
</dt> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento de instalação**](install-element.md)
</dt> <dt>

[**Configurando a loja online inicial**](setting-the-initial-online-store.md)
</dt> </dl>

 

 





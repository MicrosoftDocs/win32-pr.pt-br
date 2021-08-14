---
title: Parâmetros de linha de comando de instalação para lojas online
description: Parâmetros de linha de comando de instalação para lojas online
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Windows Media Player lojas online, parâmetros de linha de comando de instalação
- lojas online, parâmetros de linha de comando de instalação
- Digite 1 lojas online, parâmetros de linha de comando de instalação
- Digite 2 lojas online, parâmetros de linha de comando de instalação
- parâmetros de linha de comando da instalação
- Windows Media Player lojas online, parâmetros de linha de comando
- lojas online, parâmetros de linha de comando
- tipo 1 lojas online, parâmetros de linha de comando
- tipo 2 lojas online, parâmetros de linha de comando
- parâmetros de linha de comando
- Windows Media Player lojas online, parâmetros
- lojas online, parâmetros
- tipo 1 lojas online, parâmetros
- tipo 2 lojas online, parâmetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff77df581b2be4b2539772065e1aabef281a4c6c931ca115a4f6331063cf2414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569297"
---
# <a name="setup-command-line-parameters-for-online-stores"></a>Parâmetros de linha de comando de instalação para lojas online

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

ao instalar o Windows Media Player 10 ou o Windows Media Player 11 no Windows XP, você pode acrescentar parâmetros de linha de comando para especificar a primeira loja online que o usuário vê.

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

uma cadeia de caracteres de consulta que Windows Media Player 10 será acrescentada à URL do documento do serviceinfo quando ele recuperar o documento online.

## <a name="remarks"></a>Comentários

para obter detalhes sobre como redistribuir Windows Media Player software com seu aplicativo, consulte [redistribuindo Windows Media Player software](redistributing-windows-media-player-software.md).

quando o computador do usuário não está conectado à Internet, as informações contidas no documento local de informações são usadas para configurar Windows Media Player para o serviço ativo inicial.

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

 

 





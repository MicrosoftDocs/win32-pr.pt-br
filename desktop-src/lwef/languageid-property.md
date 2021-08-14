---
title: Propriedade LanguageID
description: Propriedade LanguageID
ms.assetid: f57b0fa1-b3b8-49c8-b441-2a40e564d6ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13af9f7a508732444be83fd56cce2fad6c7d7a5c148e196e2c466db102d2e6e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748694"
---
# <a name="languageid-property"></a>Propriedade LanguageID

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define a ID de idioma do caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent.***Caracteres* *  **("**_CharacterID_*_"). LanguageID_* \[  =  *LanguageID*\]



Parte

Descrição

LanguageID

Um inteiro Longo que especifica a ID de idioma do caractere. A LANGID (ID de idioma) de um caractere é um valor de 16 bits definido por Windows, que consiste em uma ID de idioma primário e uma ID de idioma secundário. Os exemplos a seguir são valores para idiomas com suporte do Microsoft Agent. Para determinar o valor de outros idiomas, consulte a *documentação do SDK da plataforma*.

 

Árabe

&H0401

Italiano

&H0410

 

Basco

&H042D

Japonês

&H0411

 

Chinês (Simplificado)

&H0804

Coreano

&H0412

 

Chinês (Tradicional)

&H0404

Norueguês

&H0414

 

Croata

&H041A

Polonês

&H0415

 

Tcheco

&H0405

Português (Portugal)

&H0816

 

Dinamarquês

&H0406

Português (Brasil)

&H0416

 

Holandês

&H0413

Romeno

&H0418

 

Inglês (britânico)

&H0809

Russo

&H0419

 

Inglês (EUA)

&H0409

Eslovaco

&H041B

 

Finlandês

&H040B

Esloveno

&H0424

 

Francês

&H040C

Espanhol

&H0C0A

 

Alemão

&H0407

Sueco

&H041D

 

Grego

&H0408

Tailandês

&H041E

 

Hebraico

&H040D

Turco

&H041F

 

Húngaro

&H040E

 

 



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você não definir o **LanguageID** para o caractere, sua ID de idioma será a ID de idioma do sistema atual se a DLL de idioma do Agent correspondente estiver instalada; caso contrário, o idioma do caractere será Inglês (EUA).

Essa propriedade também determina o idioma do texto de balão de palavras, os comandos no menu pop-up do caractere e o mecanismo de reconhecimento de fala. Ele também determina o idioma padrão para a saída do TTS.

Se você tentar definir **LanguageID** para um caractere e a DLL de idioma do Agent para esse idioma não estiver instalada ou se uma fonte de exibição para a ID do idioma não estiver disponível, o Agent gera um erro e **LanguageID** permanecerá em sua última configuração.

Definir essa propriedade não gera um erro se não houver mecanismos de fala correspondentes para o idioma. Para determinar se há um mecanismo de fala compatível disponível para **LanguageID,** verifique [**SRModeID**](srmodeid-property.md) ou [**TTSModeID**](ttsmodeid-property.md). Se você não definir **LanguageID,** ele será definido como a configuração de ID de idioma padrão do usuário.

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

> [!Note]  
> Se você definir **LanguageID** como um idioma que dá suporte a texto bidirecional (como árabe ou hebraico), mas o sistema que executa seu aplicativo não tiver suporte bidirecional instalado, o texto na palavra balão aparecerá em ordem lógica em vez de exibição.

 

## <a name="see-also"></a>Consulte Também

[**Propriedade SRModeID**](srmodeid-property.md), [ **propriedade TTSModeID**](ttsmodeid-property.md)


 

 





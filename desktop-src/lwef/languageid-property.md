---
title: Propriedade LanguageID
description: Propriedade LanguageID
ms.assetid: f57b0fa1-b3b8-49c8-b441-2a40e564d6ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7a10e6b16f9e35b223bada728871d253685538
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292688"
---
# <a name="languageid-property"></a>Propriedade LanguageID

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define a ID de idioma do caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agent. * * * caracteres* *  **("***Characterid***"). Idioma da linguagemid** \[  =  \]



Parte

Descrição

LanguageID

Um inteiro longo que especifica a ID de idioma para o caractere. A ID de idioma (LANGid) para um caractere é um valor de 16 bits definido pelo Windows, que consiste em uma ID de idioma primário e uma ID de idioma secundário. Os exemplos a seguir são valores para idiomas com suporte pelo Microsoft Agent. Para determinar o valor de outros idiomas, consulte a *documentação do Platform SDK*.

 

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

Se você não definir **LanguageID** para o caractere, sua ID de idioma será a ID de idioma do sistema atual se a DLL do idioma do agente correspondente estiver instalada, caso contrário, o idioma do caractere será inglês (EUA).

Essa propriedade também determina o idioma do texto de balão do Word, os comandos no menu pop-up do caractere e o mecanismo de reconhecimento de fala. Ele também determina o idioma padrão para a saída de TTS.

Se você tentar definir **LanguageID** para um caractere e a DLL de idioma do agente para esse idioma não estiver instalada ou uma fonte de exibição para a ID do idioma não estiver disponível, o Agent gerará um erro e **LanguageID** permanecerá em sua última configuração.

Definir essa propriedade não gerará um erro se não houver mecanismos de fala correspondentes para o idioma. Para determinar se há um mecanismo de fala compatível disponível para o **LanguageID**, verifique [**SRModeID**](srmodeid-property.md) ou [**TTSModeID**](ttsmodeid-property.md). Se você não definir **LanguageID**, ele será definido como a configuração de ID de idioma padrão do usuário.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

> [!Note]  
> Se você definir **LanguageID** como uma linguagem que dá suporte a texto bidirecional (como árabe ou Hebraico), mas o sistema executando seu aplicativo não tiver suporte bidirecional instalado, o texto na palavra balão aparecerá em lógica em vez de em ordem de exibição.

 

## <a name="see-also"></a>Consulte Também

[**Propriedade SRModeID**](srmodeid-property.md), [ **Propriedade TTSModeID**](ttsmodeid-property.md)


 

 





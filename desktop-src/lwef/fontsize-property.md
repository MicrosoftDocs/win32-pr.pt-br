---
title: Propriedade FontSize (objeto Commands)
description: Saiba mais sobre a propriedade de objeto de comandos FontSize. o Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cee9d4852a68792fe1270ebd9c91e51f567adc546433d7142de68392e9f8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751424"
---
# <a name="fontsize-property-commands-object"></a>Propriedade FontSize (objeto Commands)

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define o tamanho da fonte usado no menu pop-up do caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Caracteres Agent. ***("**_characterid_*_"). Pontos de comandos. FontSize_ *  \[  =  \]



| Parte     | Descrição                                              |
|----------|----------------------------------------------------------|
| *Faixas* | Um valor inteiro longo que especifica o tamanho da fonte em pontos. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A propriedade **FontSize** define o tamanho do ponto da fonte usada para exibir o texto no menu pop-up do caractere. O valor padrão para a configuração de fonte é baseado na configuração de fonte do menu para a configuração **LanguageID** do caractere ou — se isso não for definido — a configuração de idioma padrão do usuário.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

 

 





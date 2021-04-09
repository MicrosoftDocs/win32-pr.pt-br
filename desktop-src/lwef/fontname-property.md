---
title: Propriedade FontName (objeto Commands)
description: Propriedade FontName
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b04fa386958a75b55f9cfc50a9149de454d48f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085089"
---
# <a name="fontname-property-commands-object"></a>Propriedade FontName (objeto Commands)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define a fonte usada no menu pop-up do caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Caracteres Agent. ***("**_characterid_*_"). Fonte Commands. NomeDaFonte_ *  \[  =  \]



| Parte   | Descrição                                      |
|--------|--------------------------------------------------|
| *Fonte* | Um valor de cadeia de caracteres correspondente ao nome da fonte. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A propriedade **FontName** define a fonte usada para exibir o texto no menu pop-up do caractere. O valor padrão para a configuração fonte é baseado na configuração de fonte do menu para a configuração **LanguageID** do caractere ou, se não estiver definido, a configuração de ID de idioma padrão do usuário.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

 

 





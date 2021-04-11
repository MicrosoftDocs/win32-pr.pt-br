---
title: Propriedade Description (recursos de ambiente herdado do Windows)
description: Propriedade Description
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4fb60b20a57f56a914c7e44ced957d91bf7085
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008700"
---
# <a name="description-property-legacy-windows-environment-features"></a>Propriedade Description (recursos de ambiente herdado do Windows)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define uma cadeia de caracteres que especifica a descrição do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente* do. **Caracteres ("**_characterid_*_")._* \[  =  *Cadeia de caracteres* de descrição\]



| Parte     | Descrição                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| *cadeia de caracteres* | Um valor de cadeia de caracteres correspondente à descrição do caractere (na configuração de idioma atual). |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A **Descrição** de um caractere pode depender da configuração **LanguageID** do caractere. O nome de um caractere em um idioma pode ser diferente ou usar caracteres diferentes do que em outro. A **Descrição** padrão do caractere para um idioma específico é definida quando o caractere é compilado com o editor de caracteres do Microsoft Agent.

> [!Note]  
> A configuração da propriedade **Descrição** é opcional e pode não ser fornecida para todos os caracteres.

 

 

 





---
title: Propriedade FontCharSet
description: Propriedade FontCharSet
ms.assetid: 2f23a242-d620-4766-8f59-cf158aa55969
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4561de9af823b4213266a93b7bfa2e29588c3c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292677"
---
# <a name="fontcharset-property"></a>Propriedade FontCharSet

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define o conjunto de caracteres para a fonte exibida no balão de palavras do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid * * *"). Valor de Balloon. FontCharSet* *  \[  =  \]



| Parte    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *value* | Um valor inteiro que especifica o conjunto de caracteres usado pela fonte. A seguir estão algumas configurações comuns para valor: 0 caracteres padrão do Windows (ANSI).<br/> 1 conjunto de caracteres padrão.<br/> 2 o conjunto de caracteres do símbolo.<br/> 128 conjunto de caracteres de byte duplo (DBCS) exclusivo para a versão japonesa do Windows.<br/> 129 conjunto de caracteres de byte duplo (DBCS) exclusivo para a versão coreana do Windows.<br/> 134 conjunto de caracteres de byte duplo (DBCS) exclusivo para a versão em chinês simplificado do Windows.<br/> 136 conjunto de caracteres de dois bytes (DBCS) exclusivo para a versão em Chinês tradicional do Windows.<br/> 255 caracteres estendidos normalmente exibidos por aplicativos do Microsoft MS-DOS.<br/> Para outros valores de conjunto de caracteres, consulte a documentação do Platform SDK.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O valor padrão do conjunto de caracteres do balão de palavras de um caractere é definido no editor de caracteres do Microsoft Agent. Além disso, o usuário pode substituir as configurações de conjunto de caracteres para todos os caracteres na folha de propriedades do Microsoft Agent.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

> [!Note]  
> Se você estiver usando um caractere que não foi compilado, verifique as propriedades [**NomeDaFonte**](fontname-property.md) e **FontCharSet** do caractere para determinar se elas são apropriadas para sua localidade. Talvez seja necessário definir esses valores antes de usar o método [**Speak**](speak-method.md) para garantir a exibição de texto apropriada dentro da palavra balão.

 

## <a name="see-also"></a>Consulte Também

[**Propriedade FontName**](fontname-property.md)


 

 






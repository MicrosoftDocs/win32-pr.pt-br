---
description: Alterações de classificação de NLS
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: Alterações de classificação de NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08f0cde98d115c129fdb7932ff3bb05063cb5c6fb8d903d55bff2a69753d774
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994876"
---
# <a name="nls-sorting-changes"></a>Alterações de classificação de NLS

## <a name="affected-platforms"></a>Plataformas afetadas

 **Clientes** – Windows XP, Windows Vista, Windows 7  
**Servidores** – Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  










## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** – Alta  
**Frequência** – Baixa (alguns aplicativos afetados, mas se afetados, sempre desfeitos)  


## <a name="description"></a>Descrição

As funções de NLS (National Language Support) ajudam os aplicativos a dar suporte às diferentes necessidades específicas de idioma e localidade de usuários em todo o mundo. As Windows novas versões incluem alterações de NLS quase invariavelmente. Essa alteração afeta ordenação e classificação e, portanto, aplicativos que têm índices persistentes.

Uma tabela de collation tem dois números que identificam sua versão (revisão): a versão definida e a versão NLS. Ambas as versões são valores DWORD, compostos por uma versão principal e uma versão secundária. O primeiro byte de um valor é reservado, os próximos dois bytes representam a versão principal e o último byte representa a versão secundária. Em termos hexadecimais, o padrão é 0xRRMMMMmm, em que R é igual a Reservado, M é igual a principal e m é menor. Por exemplo, uma versão principal de 3 com uma versão secundária de 4 é representada como 0x304.

Para uma versão principal, um ou mais pontos de código mudam para que o aplicativo deve indexar todos os dados para que as comparações sejam válidas. Para uma versão secundária, nada se move, mas os pontos de código são adicionados. Para esse tipo de versão, o aplicativo só precisa indexar as cadeias de caracteres com valores anteriormente insumentáveis. Em resumo, aqui está o que os números de versão significam em relação às alterações de dados nas tabelas de exceção específicas da localidade e nas tabelas padrão:

**NLSVersion Major** – pontos de código alterados nas tabelas de "exceção" ou específicas da localidade  
**NLSVersion Minor** – adicionados novos pontos de código nas tabelas "exception" ou específicas à localidade  
**DefinedVersion Major** – pontos de código alterados na tabela padrão  
**DefinedVersion Minor** – adicionados novos pontos de código na tabela padrão  


**Classificação de números de versão para versões lançadas:**



| Sistema operacional    | Versão           | Versão (0xRRMMMMmm)         |
|---------------------|-------------------|------------------------------|
| Windows XP          | RTM/SP1/SP2/SP3/... | N/A – nenhuma API GetNLSVersion() |
| Windows Server 2003 | RTM/SP1           | 0x00 0000 01                 |
| Windows Vista       | RTM/SP1           | 0x00 0405 00                 |
| Windows Server 2008 | RTM               | 0x00 0501 00/0x00 5001 00  |
| Windows 7           | RTM               | 0x00060100                   |



 

## <a name="manifestation"></a>Manifestação

Aplicativos (como bancos de dados) com índices persistentes que não verificam a versão do NLS e re indexam após a alteração de versão falharão ao classificar corretamente ou poderão não fornecer os resultados solicitados.

No caso de interfaces do usuário, as listas (por exemplo, alfabética, numérica, alfanumérica, símbolos e assim por diante) podem ser classificação incorreta.

## <a name="solution"></a>Solução

Seu aplicativo pode chamar **GetNLSVersionEx** (Windows Vista ou posterior) ou **GetNLSVersion** (antes do Windows Vista) para recuperar a versão definida e a versão NLS para uma tabela de classificação.

-   GetNLSVersionEx:

*Recupera informações sobre a versão atual de uma funcionalidade NLS especificada para uma localidade especificada pelo nome*  
Essa função permite que um aplicativo como o Active Directory determine se uma alteração de NLS afeta a localidade usada para uma tabela de índice específica. Caso não faça isso, não será necessário indexar a tabela. Para obter mais informações, consulte Manipulando informações de localidade e idioma.  
Essa função dá suporte a localidades personalizadas. Se *lpLocaleName* especificar uma localidade suplementar, os dados recuperados serão os dados corretos para a ordem de collação associada a essa localidade suplementar.  

**Observação:** As versões Windows anteriores ao Windows Vista não são suportadas **por GetNLSVersionEx.**  


-   GetNLSVersion (use para aplicativos em execução em versões do Windows antes do Windows Vista):

*Recupera informações sobre a versão atual de uma funcionalidade NLS especificada para uma localidade especificada pelo identificador*  
Essa função permite que um aplicativo como o Active Directory determine se uma alteração de NLS afeta o identificador de localidade usado para uma tabela de índice específica. Caso não faça isso, não será necessário indexar a tabela. Para obter mais informações, consulte Manipulando informações de localidade e idioma.  
**Observação:** Essa função recupera informações apenas sobre uma localidade especificada pelo identificador. A **função GetNLSVersionEx** dá suporte a localidades, recursos e nomes RFC 4646 adicionais. No entanto, as versões Windows anteriores ao Windows Vista não são suportadas **por GetNLSVersionEx.**  
Os aplicativos destinados a ser executados somente no Windows Vista e posteriores devem usar **GetNLSVersionEx** como preferência para essa função. **GetNLSVersionEx** fornece bom suporte para localidades complementares.  


## <a name="compatibility-test"></a>Teste de compatibilidade

**Etapas para saber se uma versão de collation foi alterada (ou seja, você precisa indexar de novo):**

-   **Use GetNLSVersionEx()** para recuperar uma estrutura **NLSVERSIONINFOEX** ao fazer a indexação original de seus dados.
-   Armazene as seguintes propriedades com o índice para identificar a versão:  **NLSVERSIONINFOEX.dwNLSVersion** e **NLSVERSIONINFOEX.dwDefinedVersion** – essas duas propriedades juntas especificam a versão da tabela de classificação que você está usando.  
    **NLSVERSIONINFOEX.dwEffectiveId** – especifica a localidade efetiva de sua classificação. Uma localidade personalizada apontará para a classificação de uma localidade in-box.  
    
-   Ao usar o índice, use **GetNlsVersionEx()** para descobrir a versão de seus dados.
-   Se qualquer uma das três propriedades tiver sido alterada, os dados de classificação que você está usando poderão retornar resultados diferentes e qualquer indexação que você tiver poderá falhar ao encontrar registros.
-   Se você SABE que seus dados não contêm pontos de código Unicode inválidos (ou seja, todas as cadeias de caracteres retornaram **TRUE** de uma chamada para **IsNLSDefinedString()**), você poderá considerá-los da mesma forma se APENAS o byte baixo de **dwNLSVersion** e **dwDefinedVersion** for alterado (as versões secundárias descritas acima).

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Internacionalização para aplicativos do Windows](../intl/international-support.md)
-   [Função GetNLSVersionEx](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [Função GetNLSVersion](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [Como saber se a versão de collation foi alterada](/archive/blogs/shawnste/)

 

 

---
description: .
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: Alterações de classificação NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa4935a6874e28270e73904eb352cd6332e650b7
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314949"
---
# <a name="nls-sorting-changes"></a>Alterações de classificação NLS

## <a name="affected-platforms"></a>Plataformas afetadas

 **Clientes** -Windows XP, Windows Vista, Windows 7  
**Servidores** -windows Server 2003, windows Server 2008, windows Server 2008 R2  










## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -alta  
**Frequência** -baixa (poucos aplicativos impactados, mas se impactado, sempre interrompido)  


## <a name="description"></a>Descrição

As funções NLS (suporte ao idioma nacional) ajudam os aplicativos a dar suporte às diferentes necessidades específicas de idioma e localidade de usuários em todo o mundo. As novas versões do Windows quase invariavelmente incluem alterações de NLS. Essa alteração afeta agrupamento e classificação e, portanto, aplicativos que têm índices persistentes.

Uma tabela de agrupamento tem dois números que identificam sua versão (revisão): a versão definida e a versão do NLS. Ambas as versões são valores DWORD, compostos de uma versão principal e uma versão secundária. O primeiro byte de um valor é reservado, os próximos dois bytes representam a versão principal e o último byte representa a versão secundária. Em termos hexadecimais, o padrão é 0xRRMMMMmm, em que R é igual a reservado, M é igual a Major e m é igual a Minor. Por exemplo, uma versão principal de 3 com uma versão secundária de 4 é representada como 0x304.

Para uma versão principal, um ou mais pontos de código são alterados para que o aplicativo precise indexar novamente todos os dados para que as comparações sejam válidas. Para uma versão secundária, nada se move, mas os pontos de código são adicionados. Para esse tipo de versão, o aplicativo precisa apenas reindexar cadeias de caracteres com valores não classificados anteriormente. Em resumo, aqui está o que os números de versão significam em relação às alterações de dados nas tabelas de exceção específicas de localidade e tabelas padrão:

**NLSVersion principal** – pontos de código alterados nas tabelas ' Exception, ' ou específicas de localidade  
**NLSVersion Minor** – adicionou novos pontos de código nas tabelas ' Exception, ' ou específicas de localidade  
**DefinedVersion principal** – pontos de código alterados na tabela padrão  
**DefinedVersion Minor** – adicionou novos pontos de código na tabela padrão  


**Classificando números de versão para versões liberadas:**



| Sistema operacional    | Versão           | Versão (0xRRMMMMmm)         |
|---------------------|-------------------|------------------------------|
| Windows XP          | RTM/SP1/SP2/SP3/... | N/A-sem API GetNLSVersion () |
| Windows Server 2003 | RTM/SP1           | 0x00 0000 01                 |
| Windows Vista       | RTM/SP1           | 0x00 0405 00                 |
| Windows Server 2008 | RTM               | 0x00 0501 00/0x00 5001 00  |
| Windows 7           | RTM               | 0x00060100                   |



 

## <a name="manifestation"></a>Manifestação

Aplicativos (como bancos de dados) com índices persistentes que não verificam a versão NLS e reindexam após a alteração da versão não serão classificados corretamente ou poderão falhar em fornecer os resultados solicitados.

No caso de interfaces do usuário, as listas (por exemplo, alfabéticos, numéricos, alfanuméricos, símbolos e assim por diante) podem ser classificadas incorretamente.

## <a name="solution"></a>Solução

Seu aplicativo pode chamar **GetNLSVersionEx** (Windows Vista ou posterior) ou **GetNLSVersion** (antes do Windows Vista) para recuperar a versão definida e a versão do NLS para uma tabela de agrupamento.

-   GetNLSVersionEx:

*Recupera informações sobre a versão atual de um recurso NLS especificado para uma localidade especificada pelo nome*  
Essa função permite que um aplicativo como Active Directory determine se uma alteração NLS afeta a localidade usada para uma tabela de índice específica. Se não tiver, não será necessário reindexar a tabela. Para obter mais informações, consulte Manipulando informações de localidade e idioma.  
Essa função dá suporte a localidades personalizadas. Se *lpLocaleName* especificar uma localidade suplementar, os dados recuperados serão os dados corretos para a ordem de agrupamento associada a essa localidade complementar.  

**Observação:** Versões do Windows anteriores ao Windows Vista não dão suporte a **GetNLSVersionEx**.  


-   GetNLSVersion (use para aplicativos executados em versões do Windows anteriores ao Windows Vista):

*Recupera informações sobre a versão atual de um recurso NLS especificado para uma localidade especificada pelo identificador*  
Essa função permite que um aplicativo como Active Directory determine se uma alteração NLS afeta o identificador de localidade usado para uma tabela de índice específica. Se não tiver, não será necessário reindexar a tabela. Para obter mais informações, consulte Manipulando informações de localidade e idioma.  
**Observação:** Essa função recupera informações apenas sobre uma localidade especificada pelo identificador. A função **GetNLSVersionEx** dá suporte a localidades adicionais, recursos e nomes RFC 4646. No entanto, as versões do Windows anteriores ao Windows Vista não dão suporte a **GetNLSVersionEx**.  
Os aplicativos destinam-se a ser executados somente no Windows Vista e posterior devem usar **GetNLSVersionEx** em preferência para essa função. O **GetNLSVersionEx** fornece um bom suporte para localidades complementares.  


## <a name="compatibility-test"></a>Teste de compatibilidade

**Etapas para saber se uma versão de agrupamento foi alterada (ou seja, você precisa reindexar):**

-   **Use GetNLSVersionEx ()** para recuperar uma estrutura **NLSVERSIONINFOEX** ao fazer a indexação original de seus dados.
-   Armazene as seguintes propriedades com seu índice para identificar a versão:  **NLSVERSIONINFOEX. dwNLSVersion** e **NLSVERSIONINFOEX. dwDefinedVersion** – essas duas propriedades juntas especificam a versão da tabela de classificação que você está usando.  
    **NLSVERSIONINFOEX. dwEffectiveId** -especifica a localidade efetiva do seu tipo. Uma localidade personalizada apontará para uma classificação de localidade na caixa.  
    
-   Ao usar o índice, use **GetNlsVersionEx ()** para descobrir a versão dos seus dados.
-   Se qualquer uma das três propriedades for alterada, os dados de classificação que você está usando podem retornar resultados diferentes e qualquer indexação que você tenha pode falhar ao localizar registros.
-   Se você souber que seus dados não contêm pontos de código Unicode inválidos (ou seja, todas as cadeias de caracteres retornadas **true** de uma chamada para **IsNLSDefinedString ()**), você poderá considerá-los os mesmos se apenas o byte baixo de **dwNLSVersion** e **dwDefinedVersion** forem alterados (as versões secundárias descritas acima).

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Internacionalização para aplicativos do Windows](../intl/international-support.md)
-   [Função GetNLSVersionEx](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [Função GetNLSVersion](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [Como saber se a versão do agrupamento foi alterada](/archive/blogs/shawnste/)

 

 

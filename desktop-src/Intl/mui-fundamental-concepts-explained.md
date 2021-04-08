---
description: Conceitos fundamentais do MUI explicados
ms.assetid: 9ab19a56-4d31-471d-949e-a539751b62e3
title: Conceitos fundamentais do MUI explicados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dbeedb246944bef6c23c739eafddff86423b35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921161"
---
# <a name="mui-fundamental-concepts-explained"></a>Conceitos fundamentais do MUI explicados

-   [Pré-requisito para o MUI](#prerequisite-for-mui)
-   [Separação do código-fonte de recursos específicos do idioma](#separation-of-source-code-from-language-specific-resources)
    -   [Os primórdios: o código e os recursos residem juntos](#the-early-days-code-and-resources-live-together)
    -   [Separando logicamente o código e os recursos localizáveis](#logically-separating-code-and-localizable-resources)
    -   [Separar fisicamente o código e os recursos](#physically-separating-code-and-resources)
-   [Carregando dinamicamente recursos específicos do idioma](#dynamically-loading-language-specific-resources)
-   [Criando aplicativos MUI](#building-mui-applications)

## <a name="prerequisite-for-mui"></a>Pré-requisito para o MUI

O pré-requisito básico para a criação de um aplicativo compatível com MUI para o Windows Vista e posterior é projetar o aplicativo de acordo com as [diretrizes de globalização](https://msdn.microsoft.com/goglobal/bb688110.aspx)do Windows.

## <a name="separation-of-source-code-from-language-specific-resources"></a>Separação do código-fonte de recursos específicos do idioma

Um dos locais fundamentais da tecnologia MUI é a separação do código-fonte do aplicativo dos recursos específicos do idioma, para permitir cenários de vários idiomas em aplicativos com mais eficiência. A separação do código e dos recursos foi obtida por meio de diferentes mecanismos e para diferentes graus ao longo do tempo, conforme descrito nas seções a seguir. Cada método forneceu graus variados de flexibilidade na criação, implantação e manutenção do aplicativo.

A solução recomendada para aplicativos em conformidade com o MUI é o último método descrito aqui, ou seja, a separação física do código-fonte do aplicativo e dos recursos, com os próprios recursos divididos em um arquivo por idioma com suporte para obter a máxima flexibilidade na criação, implantação e manutenção.

### <a name="the-early-days-code-and-resources-live-together"></a>Os primórdios: o código e os recursos residem juntos

Inicialmente, os aplicativos localizados foram criados editando-se o código-fonte e alterando os recursos (geralmente cadeias de caracteres) no próprio código e recompilando os aplicativos. Isso significava que, para produzir uma versão localizada, era necessário copiar o código-fonte original, converter os elementos de texto (recursos) no código-fonte e recompilar o código. A imagem a seguir mostra o código do aplicativo com texto que precisa ser localizado.

![diagrama conceitual mostrando um aplicativo que contém unidades de recursos de texto inseridos](images/mui-fundamental-concepts-explained-fig3.gif)

Embora essa abordagem permita a criação de aplicativos localizados, ela também tem desvantagens significativas:

-   Ele requer várias versões do código-fonte, pelo menos uma para o idioma de origem e outra para cada um dos idiomas de destino. Isso cria problemas significativos na sincronização das diferentes versões de idioma do aplicativo. Em particular, quando um defeito precisa ser corrigido no código, o defeito precisa ser corrigido em cada cópia do código-fonte (um por idioma).
-   Ele também é extremamente propenso a erros que os localizadores exigidos por eles, que não são desenvolvedores, para fazer modificações no código-fonte, criando, assim, um risco considerável em termos de integridade de código.

A combinação dessas desvantagens torna essa uma proposta extremamente ineficiente, e um modelo melhor era necessário.

### <a name="logically-separating-code-and-localizable-resources"></a>Separando logicamente o código e os recursos localizáveis

Uma melhoria significativa sobre o modelo anterior é a separação lógica de código e recursos localizáveis para um aplicativo. Isso isola o código dos recursos e garante que o código permaneça inalterado quando os recursos estiverem sendo alterados pela localização. Do ponto de vista da implementação, cadeias de caracteres e outros elementos da interface do usuário são armazenados em arquivos de recursos, que são relativamente fáceis de traduzir e são separados logicamente das seções de código.

O ideal é que adicionar suporte a qualquer linguagem pode ser tão simples quanto converter os recursos localizáveis nessa nova linguagem e usar esses recursos traduzidos para criar uma nova versão localizada do aplicativo, sem a necessidade de qualquer modificação de código. A imagem a seguir ilustra como o código e os recursos localizáveis devem ser separados logicamente em um aplicativo.

![diagrama conceitual que mostra um aplicativo que contém recursos localizáveis separados do código](images/mui-fundamental-concepts-explained-fig4.gif)

Esse modelo permite uma criação mais fácil de versões localizadas de um aplicativo e é uma melhoria significativa em relação ao modelo anterior. Esse modelo, implementado com o uso de ferramentas de gerenciamento de recursos, foi muito bem-sucedido ao longo dos anos e ainda é normalmente usado por muitos aplicativos atualmente. No entanto, ela tem desvantagens significativas:

-   Enquanto separados logicamente, o código e os recursos localizados ainda são fisicamente ingressados em um arquivo executável. Em particular, a manutenção ainda é problemática, pois o mesmo defeito de código (idêntico em todas as versões de idioma) requer um patch por idioma. Portanto, se um estiver enviando o aplicativo em 20 idiomas, um patch de serviço precisará ser emitido 20 vezes (um para cada idioma), mesmo que o código seja corrigido apenas uma vez.
-   A distribuição e o uso de aplicativos multilíngües não têm suporte adequado para esse modelo. Isso pode ser um problema significativo em cenários de OEM e empresariais. Por exemplo, se um computador for compartilhado entre dois usuários usando diferentes idiomas, os aplicativos precisarão ser instalados duas vezes com esse modelo e, em seguida, um mecanismo precisará ser habilitado para alternar entre as duas instalações. Isso pressupõe que não há dependências adicionais que impeçam que até mesmo esse cenário seja implementado. A imagem a seguir mostra um exemplo de um único defeito de código que requer dois patches.

![diagrama conceitual que mostra dois aplicativos localizados que têm o mesmo código de defeito](images/mui-fundamental-concepts-explained-fig5.gif)

É claro que, embora esse modelo funcione bem em alguns cenários, suas limitações para aplicativos multilíngües e suas implantações podem ser muito problemáticas.

Uma variação desse modelo que alivia alguns dos problemas de aplicativos multilíngües é o modelo em que os recursos localizáveis contêm um conjunto de recursos de idioma diferentes. Esse modelo tem uma base de código comum e vários recursos para diferentes idiomas no mesmo aplicativo. Por exemplo, um aplicativo pode ser enviado com inglês, alemão, francês, espanhol, holandês e italiano no mesmo pacote. A imagem a seguir mostra um aplicativo que contém vários recursos de idioma.

![diagrama conceitual mostrando um aplicativo com código separado de dois recursos específicos de localidade](images/mui-fundamental-concepts-explained-fig6.gif)

Esse modelo facilita a manutenção do aplicativo quando um defeito de código precisa ser corrigido, o que é um aperfeiçoamento, mas não melhora os modelos anteriores quando se trata de dar suporte a idiomas adicionais. Nesse caso, uma ainda precisa lançar uma nova versão do aplicativo (e essa versão é potencialmente complicada pela necessidade de garantir que todos os recursos de idioma sejam sincronizados na mesma distribuição).

### <a name="physically-separating-code-and-resources"></a>Separar fisicamente o código e os recursos

A próxima etapa evolucionário é separar fisicamente o código e os recursos. Nesse modelo, os recursos são dissociados do código e fisicamente separados em arquivos de implementação diferentes. Em particular, isso significa que o código pode se tornar verdadeiramente independente de linguagem; o mesmo código físico é enviado de fato para todas as versões localizadas de um aplicativo. A imagem a seguir ilustra que o código e os recursos localizáveis devem ser separados fisicamente.

![diagrama conceitual que mostra um aplicativo separado de seus recursos localizáveis](images/mui-fundamental-concepts-explained-fig7.gif)

Essa abordagem tem várias vantagens em relação às abordagens anteriores:

-   A implantação de soluções multilíngues é bastante simplificada. Adicionar suporte a qualquer linguagem específica requer apenas o envio e a instalação de um novo conjunto de recursos de idioma para esse idioma específico. Isso é particularmente importante quando os recursos de idioma não estão todos disponíveis simultaneamente. Com esse modelo, é possível implantar um aplicativo em um conjunto de idiomas principais e aumentar o número de idiomas com suporte ao longo do tempo sem precisar modificar ou reimplantar o código real. Essa vantagem é ainda mais estendida por um mecanismo de fallback que permite a localização parcial de aplicativos e componentes do sistema em um determinado idioma, garantindo que os recursos não encontrados nesse idioma preferencial "voltem" para outro idioma que os usuários também compreendam. Em geral, esse modelo ajuda a aliviar a sobrecarga considerável que as empresas globais enfrentam na implantação de aplicativos em várias linguagens, pois permite a implantação de imagem única de maneira muito mais eficiente.
-   A manutenção é aprimorada. Um defeito de código só precisa ser corrigido e implantado uma vez, pois o código é totalmente independente de localização. Com esse modelo, emitir uma correção para um defeito de código, desde que a alteração não seja relacionada à interface do usuário, é muito mais simples e econômica do que em qualquer um dos modelos anteriores.

## <a name="dynamically-loading-language-specific-resources"></a>Carregando dinamicamente recursos específicos do idioma

Os conceitos fundamentais do MUI de [separar fisicamente o código-fonte de recursos específicos do idioma](#physically-separating-code-and-resources)e a criação de um binário principal com neutralidade de idioma para um aplicativo, essencialmente definem uma arquitetura que conduz a implementação do carregamento dinâmico de recursos específicos de linguagem com base nas configurações de idioma do usuário e do sistema.

O código-fonte do aplicativo agrupado no binário principal com neutralidade de idioma pode utilizar APIs do MUI na plataforma Windows para abstrair a seleção do idioma de interface do usuário de exibição apropriado para um determinado contexto. O MUI dá suporte a isso:

-   Construindo uma lista priorizada de exibir idiomas de interface do usuário com base nas configurações de nível de sistema, usuário e nível de aplicativo, nível de usuário e sistema.
-   Implementação de um mecanismo de fallback que escolhe um candidato apropriado a partir dessa lista priorizada de idiomas, com base na disponibilidade de recursos localizados.

Os benefícios de carregar dinamicamente recursos de interface do usuário com fallback prioritário são:

-   Ele permite a localização parcial de aplicativos e componentes do sistema em um determinado idioma, já que os recursos que não são encontrados nesse idioma preferencial serão automaticamente devolvidos para o próximo idioma na lista de prioridades.
-   Ele permite cenários como alternar dinamicamente de um idioma para outro.
-   Ele permite a criação de imagens de implantação única regionais ou mundiais que abrangem um conjunto de idiomas para OEMs e empresas.

## <a name="building-mui-applications"></a>Criando aplicativos MUI

As seções anteriores descreveram as opções para separar o código-fonte de recursos específicos do idioma e o benefício resultante na capacidade de utilizar as principais APIs da plataforma Windows para carregar dinamicamente os recursos localizados. Embora essas sejam diretrizes, também deve-se destacar que não há uma maneira prescritiva específica de desenvolver um aplicativo MUI para a plataforma Windows.

Os desenvolvedores de aplicativos têm a opção completa de como lidar com várias configurações de idioma de interface do usuário, opções de criação de recursos e métodos de carregamento de recursos. Os desenvolvedores podem avaliar as diretrizes fornecidas neste documento e escolher uma combinação que atenda às suas necessidades e ao ambiente de desenvolvimento.

A tabela a seguir resume as diferentes opções de design disponíveis para desenvolvedores de aplicativos que estão procurando criar um aplicativo MUI para a plataforma Windows.



<table>
<thead>
<tr class="header">
<th>Configurações de idioma da interface do usuário</th>
<th>Criação de recursos</th>
<th>Carregamento de recursos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">Siga as configurações de idioma da interface do usuário no sistema operacional $ {REMOVE} $<br />
</td>
<td>Idioma único em um recurso de divisão binário (tecnologia de recurso do MUI)<br/> – ou –<br/> Vários idiomas em um binário de recursos não divididos<br/></td>
<td>O aplicativo chama funções de carregamento de recurso padrão. Os recursos são retornados nos idiomas correspondentes às configurações do sistema operacional.<br/></td>
</tr>
<tr class="even">
<td>Mecanismo de recursos específico do aplicativo<br/></td>
<td>O aplicativo chama a API do MUI para recuperar os idiomas da interface do usuário preferenciais do thread ou os idiomas da interface do usuário de preferência do processo do sistema operacional e usar essas configurações para carregar seus próprios recursos.<br/></td>

</tr>
<tr class="odd">
<td rowspan="2">Configurações de idioma da interface do usuário específica do aplicativo $ {REMOVE} $<br />
</td>
<td>Idioma único em um binário de recurso de divisão<br/> – ou –<br/> Vários idiomas em um binário de recursos não divididos<br/></td>
<td>O aplicativo chama a API do MUI para definir idiomas de interface do usuário específicos do aplicativo ou linguagens de interface do usuário de processo e, em seguida, chama funções de carregamento de recursos Os recursos são retornados nos idiomas definidos pelo aplicativo ou pelos idiomas do sistema.<br/> – ou –<br/> O aplicativo investiga recursos em uma linguagem específica e manipula sua própria extração de recursos dos dados binários recuperados.<br/></td>
</tr>
<tr class="even">
<td>Mecanismo de recursos específico do aplicativo<br/></td>
<td>O aplicativo gerencia seu próprio carregamento de recursos.<br/></td>

</tr>
</tbody>
</table>



 

 

 





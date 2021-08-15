---
description: Conceitos fundamentais da MUI explicados
ms.assetid: 9ab19a56-4d31-471d-949e-a539751b62e3
title: Conceitos fundamentais da MUI explicados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88bd677d7a6b07bc4db78d733d81fc36624ddd06f9ad3014588b8e5fd0882aa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390870"
---
# <a name="mui-fundamental-concepts-explained"></a>Conceitos fundamentais da MUI explicados

-   [Pré-requisito para a MUI](#prerequisite-for-mui)
-   [Separação do código-fonte de recursos específicos da linguagem](#separation-of-source-code-from-language-specific-resources)
    -   [Os primeiros dias: o código e os recursos estão juntos](#the-early-days-code-and-resources-live-together)
    -   [Separando logicamente o código e os recursos localizáveis](#logically-separating-code-and-localizable-resources)
    -   [Separando fisicamente o código e os recursos](#physically-separating-code-and-resources)
-   [Carregando dinamicamente recursos específicos do idioma](#dynamically-loading-language-specific-resources)
-   [Criando aplicativos de MUI](#building-mui-applications)

## <a name="prerequisite-for-mui"></a>Pré-requisito para a MUI

O pré-requisito básico para a criação de um aplicativo compatível com a MUI para o Windows Vista e além é criar o aplicativo de acordo com Windows [de globalização.](https://msdn.microsoft.com/goglobal/bb688110.aspx)

## <a name="separation-of-source-code-from-language-specific-resources"></a>Separação do código-fonte de recursos específicos da linguagem

Uma das instalações fundamentais da tecnologia de MUI é a separação do código-fonte do aplicativo de recursos específicos da linguagem, para habilitar cenários multilínguários em aplicativos com mais eficiência. A separação de código e recursos foi alcançada por meio de mecanismos diferentes e em graus diferentes ao longo do tempo, conforme descrito nas seções a seguir. Cada método forneceu graus variados de flexibilidade na criação, implantação e manutenção do aplicativo.

A solução recomendada para aplicativos em conformidade com a MUI é o último método descrito aqui, ou seja, a separação física do código-fonte do aplicativo e dos recursos, com os próprios recursos divididos ainda mais em um arquivo por idioma com suporte para máxima flexibilidade na criação, implantação e manutenção.

### <a name="the-early-days-code-and-resources-live-together"></a>Os primeiros dias: o código e os recursos estão juntos

Inicialmente, os aplicativos localizados foram criados editando o código-fonte e alterando os recursos (geralmente cadeias de caracteres) no próprio código e recompilando os aplicativos. Isso significa que, para produzir uma versão localizada, era necessário copiar o código-fonte original, traduzir os elementos de texto (recursos) dentro do código-fonte e recompilar o código. A imagem a seguir mostra o código do aplicativo com texto que precisa ser localizado.

![diagrama conceitual mostrando um aplicativo que contém unidades de recursos de texto inseridos](images/mui-fundamental-concepts-explained-fig3.gif)

Embora essa abordagem habilita a criação de aplicativos localizados, ela também tem desvantagens significativas:

-   Ele requer várias versões do código-fonte, pelo menos uma para o idioma de origem e outra para cada um dos idiomas de destino. Isso cria problemas significativos na sincronização das diferentes versões de idioma do aplicativo. Em particular, quando um defeito precisa ser corrigido no código, o defeito precisa ser corrigido em cada cópia do código-fonte (uma por idioma).
-   Também é extremamente propenso a erros, pois é necessário que os localizadores , que não são desenvolvedores, façam modificações no código-fonte, criando um risco considerável em termos de integridade do código.

A combinação dessas desvantagens torna essa proposta extremamente ineficiente e um modelo melhor era necessário.

### <a name="logically-separating-code-and-localizable-resources"></a>Separando logicamente o código e os recursos localizáveis

Uma melhoria significativa em relação ao modelo anterior é a separação lógica de código e recursos localizáveis para um aplicativo. Isso isola o código dos recursos e garante que o código permaneça inalterado quando os recursos estão sendo alterados pela localização. Do ponto de vista da implementação, cadeias de caracteres e outros elementos de interface do usuário são armazenados em arquivos de recurso, que são relativamente fáceis de traduzir e são logicamente separados das seções de código.

Idealmente, adicionar suporte para qualquer idioma pode ser tão simples quanto traduzir os recursos localizáveis para esse novo idioma e usar esses recursos traduzidos para criar uma nova versão localizada do aplicativo, sem exigir nenhuma modificação de código. A imagem a seguir ilustra como o código e os recursos localizáveis devem ser separados logicamente dentro de um aplicativo.

![diagrama conceitual que mostra um aplicativo que contém recursos localizáveis separados do código](images/mui-fundamental-concepts-explained-fig4.gif)

Esse modelo permite uma criação mais fácil de versões localizadas de um aplicativo e é uma melhoria significativa em relação ao modelo anterior. Esse modelo, implementado por meio do uso de ferramentas de gerenciamento de recursos, tem sido muito bem-sucedido ao longo dos anos e ainda é normalmente usado por muitos aplicativos atualmente. No entanto, ele tem desvantagens significativas:

-   Embora separados logicamente, o código e os recursos localizados ainda são fisicamente unidos em um arquivo executável. Em particular, a capacidade de serviço ainda é problemática, pois o mesmo defeito de código (idêntico em todas as versões de idioma) requer um patch por idioma. Portanto, se um estiver enviando o aplicativo em 20 idiomas, um patch de serviço precisará ser emitido 20 vezes (um para cada idioma), mesmo que o código seja corrigido apenas uma vez.
-   Não há suporte adequado para a distribuição e o uso de aplicativos multilínguário por esse modelo. Isso pode ser um problema significativo em cenários OEM e empresariais. Por exemplo, se um computador deve ser compartilhado entre dois usuários usando idiomas diferentes, os aplicativos precisarão ser instalados duas vezes com esse modelo e, em seguida, algum mecanismo precisará ser habilitado para alternar entre as duas instalações. Isso pressu que não há dependências adicionais que impeçam até mesmo que esse cenário seja implementado. A imagem a seguir mostra um exemplo de um único defeito de código que requer dois patches.

![diagrama conceitual que mostra dois aplicativos localizados que têm o mesmo defeito de código](images/mui-fundamental-concepts-explained-fig5.gif)

É claro que, embora esse modelo funcione bem em alguns cenários, suas limitações para aplicativos multilínguário e suas implantações podem ser muito problemáticas.

Uma variação desse modelo que alivia alguns dos problemas de aplicativos multilínguários é o modelo em que os recursos localizáveis contêm um conjunto de recursos de linguagem diferentes. Esse modelo tem uma base de código comum e vários recursos para idiomas diferentes no mesmo aplicativo. Por exemplo, um aplicativo pode enviar com inglês, alemão, francês, espanhol, holandês e italiano no mesmo pacote. A imagem a seguir mostra um aplicativo que contém vários recursos de idioma.

![diagrama conceitual mostrando um aplicativo com código separado de dois recursos específicos da localidade](images/mui-fundamental-concepts-explained-fig6.gif)

Esse modelo facilita o serviço do aplicativo quando um defeito de código precisa ser corrigido, o que é uma melhoria, mas não melhora em relação aos modelos anteriores quando se trata de dar suporte a idiomas adicionais. Nesse caso, ainda é necessário lançar uma nova versão do aplicativo (e essa versão é potencialmente complicada pela necessidade de garantir que todos os recursos de idioma sejam sincronizados dentro da mesma distribuição).

### <a name="physically-separating-code-and-resources"></a>Separando fisicamente o código e os recursos

A próxima etapa evolutiva é separar fisicamente o código e os recursos. Nesse modelo, os recursos são abstraídos do código e fisicamente separados em arquivos de implementação diferentes. Em particular, isso significa que o código pode se tornar realmente independente de idioma; o mesmo código físico é realmente enviado para todas as versões localizadas de um aplicativo. A imagem a seguir ilustra que o código e os recursos localizáveis devem ser fisicamente separados.

![diagrama conceitual que mostra um aplicativo separado de seus recursos localizáveis](images/mui-fundamental-concepts-explained-fig7.gif)

Essa abordagem tem várias vantagens em relação às abordagens anteriores:

-   A implantação de soluções multilíndico é bastante simplificada. Adicionar suporte para qualquer idioma específico requer apenas o envio e a instalação de um novo conjunto de recursos de idioma para esse idioma específico. Isso é particularmente importante quando os recursos de idioma não estão todos disponíveis simultaneamente. Com esse modelo, é possível implantar um aplicativo em um conjunto de linguagens principais e aumentar o número de idiomas com suporte ao longo do tempo sem precisar modificar ou reimplantar o código real. Essa vantagem é estendida ainda mais por um mecanismo de fallback que permite a localização parcial de aplicativos e componentes do sistema em um determinado idioma, garantindo que os recursos que não são encontrados nesse idioma preferencial "fallback" para outro idioma que os usuários também entendam. Em geral, esse modelo ajuda a atenuar a carga considerável que as empresas globais enfrentam na implantação de aplicativos em vários idiomas, pois permite a implantação de imagem única de maneira muito mais eficaz.
-   A capacidade de serviço é aprimorada. Um defeito de código só precisa ser corrigido e implantado uma vez, pois o código é completamente independente de localização. Com esse modelo, a emissão de uma correção para um defeito de código, desde que a alteração não seja relacionada à interface do usuário, é muito mais simples e econômica do que em qualquer um dos modelos anteriores.

## <a name="dynamically-loading-language-specific-resources"></a>Carregando dinamicamente recursos específicos do idioma

Os conceitos fundamentais [](#physically-separating-code-and-resources)da MUI de separar fisicamente o código-fonte de recursos específicos de linguagem e criar um binário de núcleo neutro em idioma para um aplicativo, essencialmente configurar uma arquitetura que seja propícia para implementar o carregamento dinâmico de recursos específicos de idioma com base nas configurações de idioma do usuário e do sistema.

O código-fonte do aplicativo agrupado no binário de núcleo neutro da linguagem pode utilizar APIs de MUI na plataforma Windows para abstração da seleção da linguagem de interface do usuário de exibição apropriada para um determinado contexto. A MUI dá suporte a isso:

-   Construindo uma lista priorizada de linguagens de interface do usuário de exibição com base nas configurações no nível do sistema, do usuário e do aplicativo, no nível do usuário e no nível do sistema.
-   Implementando um mecanismo de fallback que escolhe um candidato apropriado nessa lista priorizada de idiomas, com base na disponibilidade de recursos localizados.

Os benefícios de carregar dinamicamente recursos de interface do usuário com fallback priorizado são:

-   Ele permite a localização parcial de aplicativos e componentes do sistema em um determinado idioma, pois os recursos que não são encontrados nesse idioma preferencial retornarão automaticamente para o próximo idioma na lista priorizada.
-   Ele permite cenários como alternar dinamicamente de um idioma para outro.
-   Ele permite a criação de imagens de implantação única regionais ou em todo o mundo que abrangem um conjunto de idiomas para OEMs e empresas.

## <a name="building-mui-applications"></a>Criando aplicativos de MUI

As seções anteriores delineam as opções para separar o código-fonte de recursos específicos de linguagem e o benefício resultante em poder utilizar apIs de plataforma Windows principais para carregar dinamicamente os recursos localizados. Embora essas sejam diretrizes, também deve ser apontado que não há nenhuma maneira prescritiva específica para desenvolver um aplicativo de MUI para a Windows plataforma.

Os desenvolvedores de aplicativos têm total opção em como lidam com várias configurações de linguagem de interface do usuário, opções de criação de recursos e métodos de carregamento de recursos. Os desenvolvedores podem avaliar as diretrizes fornecidas neste documento e escolher uma combinação que se ajuste aos seus requisitos e ao ambiente de desenvolvimento.

A tabela a seguir resume as diferentes opções de design disponíveis para desenvolvedores de aplicativos que estão procurando criar um aplicativo MUI para a Windows plataforma.



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
<td rowspan="2">Siga as configurações de idioma da interface do usuário no sistema operacional${REMOVE}$<br />
</td>
<td>Idioma único em um binário de recurso dividido (MUI Resource Technology)<br/> -ou-<br/> Vários idiomas em um binário de recurso não dividido<br/></td>
<td>O aplicativo chama funções de carregamento de recursos padrão. Os recursos são retornados nos idiomas correspondentes às configurações do sistema operacional.<br/></td>
</tr>
<tr class="even">
<td>Mecanismo de recurso específico do aplicativo<br/></td>
<td>O aplicativo chama a API de MUI para recuperar os idiomas de interface do usuário preferenciais por thread ou os idiomas de interface do usuário preferenciais ao processo do sistema operacional e usar essas configurações para carregar seus próprios recursos.<br/></td>

</tr>
<tr class="odd">
<td rowspan="2">Configurações de idioma da interface do usuário específicas do aplicativo${REMOVE}$<br />
</td>
<td>Idioma único em um binário de recurso dividido<br/> -ou-<br/> Vários idiomas em um binário de recursos não divididos<br/></td>
<td>O aplicativo chama a API do MUI para definir idiomas de interface do usuário específicos do aplicativo ou linguagens de interface do usuário de processo e, em seguida, chama funções de carregamento de recursos Os recursos são retornados nos idiomas definidos pelo aplicativo ou pelos idiomas do sistema.<br/> -ou-<br/> O aplicativo investiga recursos em uma linguagem específica e manipula sua própria extração de recursos dos dados binários recuperados.<br/></td>
</tr>
<tr class="even">
<td>Mecanismo de recursos específico do aplicativo<br/></td>
<td>O aplicativo gerencia seu próprio carregamento de recursos.<br/></td>

</tr>
</tbody>
</table>



 

 

 





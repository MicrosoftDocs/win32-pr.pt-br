---
description: Este tópico explica como criar e registrar manipuladores de propriedade para trabalhar com o sistema de propriedades do Windows.
ms.assetid: E6E81E04-9CC1-4df5-9A87-DE0CBD177356
title: Registrando e distribuindo manipuladores de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1de6af17df8e15912870626935995c67c25f518
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165274"
---
# <a name="registering-and-distributing-property-handlers"></a>Registrando e distribuindo manipuladores de propriedade

Este tópico explica como criar e registrar manipuladores de propriedade para trabalhar com o sistema de propriedades do Windows.

Este tópico é organizado da seguinte maneira:

-   [Registrando e distribuindo manipuladores de propriedade](#registering-and-distributing-property-handlers)
-   [Considerações de desempenho e confiabilidade para manipuladores de propriedade](#performance-and-reliability-considerations-for-property-handlers)
    -   [Diretrizes para desempenho e confiabilidade](#guidelines-for-performance-and-reliability)
-   [Tópicos relacionados](#related-topics)

## <a name="registering-and-distributing-property-handlers"></a>Registrando e distribuindo manipuladores de propriedade

Depois que o manipulador de propriedades é implementado, ele deve ser registrado e sua extensão de nome de arquivo deve ser associada ao manipulador. O exemplo a seguir usando a extensão. recipe ilustra as entradas de Registro necessárias para fazer isso.

```
HKEY_CLASSES_ROOT
   CLSID
      {50d9450f-2a80-4f08-93b9-2eb526477d1a}
         (Default) = Recipe Property Handler
         ManualSafeSave [REG_DWORD] = 00000001
         InProcServer32
            (Default) = C:\\SDK\\PropertyHandlerSample\\bin\\RecipeHandlers.dll
            ThreadingModel = Apartment
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     .recipe
                        (Default) = {50d9450f-2a80-4f08-93b9-2eb526477d1a}
```

Os manipuladores de propriedade para um determinado tipo de arquivo são normalmente distribuídos com os aplicativos que criam ou manipulam arquivos desse tipo. No entanto, você também deve considerar tornar os manipuladores de propriedade disponíveis independentemente desses aplicativos para dar suporte à indexação de seu tipo de arquivo em cenários de servidor em que os manipuladores de propriedade são usados pelo indexador, mas os aplicativos que os acompanham não são necessários. Se você criar um pacote de instalação autônoma para seu manipulador de propriedades, certifique-se de que ele inclui o seguinte:

-   Os detalhes de registro do manipulador de propriedade especificados no tópico [registrando e distribuindo manipuladores de propriedade]().
-   Registro para o tipo de arquivo e todos os arquivos de esquema que devem ser instalados, para permitir que os clientes acessem todos os recursos do manipulador de propriedades.

## <a name="performance-and-reliability-considerations-for-property-handlers"></a>Considerações de desempenho e confiabilidade para manipuladores de propriedade

Manipuladores de propriedade são invocados para cada arquivo em um computador específico. Normalmente, eles são chamados nas seguintes circunstâncias:

-   Durante a indexação do arquivo. Isso é feito fora do processo, em um processo isolado com direitos restritos.
-   Quando os arquivos são acessados no Windows Explorer com a finalidade de ler e gravar valores de propriedade. Isso é feito em processo.

### <a name="guidelines-for-performance-and-reliability"></a>Diretrizes para desempenho e confiabilidade

A qualquer momento, um usuário pode ter dezenas de milhares de arquivos de qualquer tipo específico (incluindo o seu) em seus computadores e pode acessar ou modificar um ou todos esses arquivos a qualquer momento. Como os manipuladores de propriedades são frequentemente invocados para dar suporte a essas operações de acesso e modificação, as características de desempenho e confiabilidade do manipulador de propriedades estão ocupadas, ambientes altamente simultâneos são de importância crítica.

Tenha em mente as seguintes diretrizes enquanto você está desenvolvendo e testando seu manipulador de propriedades.

-   **Enumeração de propriedade**

    Manipuladores de propriedade devem ter um tempo de resposta muito rápido para enumerar suas propriedades. Os cálculos com uso intensivo de memória de valores de propriedade, pesquisas de rede ou a pesquisa de recursos que não sejam o próprio arquivo devem ser evitados para garantir tempos de resposta rápidos.

-   **Gravação de propriedades in-loco**

    Se possível, ao lidar com arquivos médios ou grandes (várias centenas de KB ou mais), o formato de arquivo deve ser organizado de forma que a leitura ou a gravação de valores de propriedade não exija a leitura do arquivo inteiro do disco. Mesmo que o arquivo precise ser procurado, ele não deve ser lido na memória integralmente porque isso infla o conjunto de trabalho do Windows Explorer ou do indexador do Windows Search à medida que tentam acessar ou indexar esses arquivos. Para obter mais informações, consulte [inicializando manipuladores de propriedade](./building-property-handlers-property-handlers.md).

    Uma técnica útil para fazer isso é preencher o cabeçalho do arquivo com espaço extra para que na próxima vez que um valor de propriedade precise ser gravado, o valor possa ser gravado em vigor sem a necessidade de regravar o arquivo inteiro. Isso requer a funcionalidade ManualSafeSave. Essa abordagem envolve alguns riscos extras que a operação de gravação de arquivo pode ser interrompida enquanto a gravação está em andamento (devido a uma falha do sistema ou perda de energia), mas como os tamanhos de propriedades são geralmente pequenos, a probabilidade de tal interrupção é muito pequena e os ganhos de desempenho que podem ser percebidos por meio da gravação de propriedades in-loco são considerados significativos o suficiente para justificar esse risco Mesmo assim, você deve cuidar de testar sua implementação extensivamente para garantir que os arquivos não estejam corrompidos caso ocorra uma falha no decorrer de uma operação de gravação.

    Por fim, ao implementar a gravação de propriedades in-loco com ManualSafeSave, às vezes a operação não pode ser executada in-loco e todo o fluxo deve ser reescrito de qualquer forma. Para facilitar a reescrita, o fluxo fornecido durante a inicialização do manipulador dá suporte à interface [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory) . A interface **IDestinationStreamFactory** permite que as implementações de manipulador obtenham um fluxo temporário para gravação; Quando todas as gravações são concluídas e o método [**IDestinationStreamFactory:: GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream) é chamado, esse fluxo é usado para substituir completamente o fluxo de arquivos original. Quando o fluxo de destino é usado, o fluxo de arquivos original deve ser tratado como somente leitura, pois ele será substituído pelo fluxo de destino depois que o método **IDestinationStreamFactory:: GetDestinationStream** for chamado.

-   **Escolhendo seu modelo de Threading COM**

    Para maximizar a eficiência do manipulador de propriedades, você deve especificar que ele usa o modelo de Threading COM `Both` . Isso permite o acesso direto do STA Apartments (Windows Explorer, por exemplo) e do MTA (agente de transferência de mensagens) Apartments (o processo SearchProtocolHost no Windows Search, por exemplo), evitando a sobrecarga de marshaling nesses ambientes. Para obter todo o benefício do `Both` modelo de Threading, todos os serviços nos quais o manipulador depende também devem ser designados como `Both` para evitar qualquer marshaling em chamadas para esses componentes. Verifique a documentação desses serviços específicos para verificar se eles usam esse modelo de Threading.

-   **Simultaneidade do manipulador de propriedades**

    Os manipuladores de propriedade e a interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) são projetados para acesso serial em vez de simultâneo. O Windows Explorer, o indexador do Windows Search e todas as outras invocações do manipulador de propriedades da base de código do Windows garantem esse uso. Não deve haver nenhum motivo para que terceiros usem um manipulador de propriedade simultaneamente, mas esse comportamento não pode ser garantido. Além disso, embora seja esperado que o padrão de chamada seja serial, as chamadas podem vir em threads diferentes (por exemplo, quando o objeto está sendo chamado remotamente via RPC COM, como ocorre no indexador). Portanto, as implementações do manipulador de propriedades devem dar suporte à chamada em threads diferentes e, idealmente, não deve sofrer nenhum efeito inadequado quando chamado simultaneamente. Como o padrão de chamada pretendido é serial, uma implementação trivial usando uma seção crítica deve ser suficiente para atender a esses requisitos na maioria dos casos. É aceitável evitar o bloqueio em chamadas simultâneas usando a função [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) para detectar e reprovar chamadas simultâneas.

-   **Simultaneidade de arquivo**

    Manipuladores de propriedade geralmente são usados em cenários em que vários aplicativos acessam um arquivo simultaneamente. Portanto, o manipulador e os aplicativos precisam gerenciar a simultaneidade especificando os modos de compartilhamento apropriados ao abrir o arquivo. Eles também precisam estar cientes do acesso que os outros aplicativos especificam e para gerenciar casos em que o acesso não é permitido. É melhor se todos os consumidores especificarem modos de compartilhamento liberal para permitir que outras pessoas acessem o arquivo simultaneamente, mas ao fazer isso, os problemas de consistência precisam ser gerenciados. As decisões sobre os modos de compartilhamento mais apropriados a serem usados precisam ser feitas no contexto da comunidade de aplicativos que acessam o arquivo.

    Os sistemas de arquivos permitem que os aplicativos abram arquivos de forma que forneçam controle sobre se e como outros aplicativos podem abrir o arquivo. Os modos de compartilhamento habilitam o acesso de leitura, gravação e exclusão. O sistema de propriedades dá suporte a um subconjunto desses modos de compartilhamento, descrito na tabela a seguir.

    

    | Modo de acesso                     | Modo de compartilhamento                             |
    |---------------------------------|------------------------------------------|
    | Gravar                           | Negar outros leitores e gravadores           |
    | Gravação (EnableShareDenyWrite)    | Habilitar outros leitores, negar outros gravadores |
    | Somente leitura (padrão)             | Habilitar outros leitores, negar outros gravadores |
    | Somente leitura (EnableShareDenyNone) | Habilitar outros leitores e gravadores         |

    

     

    Os manipuladores de propriedade abertos para **gravação** (GPS \_ ReadWrite) negarão outros leitores e gravadores. Os manipuladores podem optar pelo comportamento que habilita os leitores especificando o `EnableShareDenyWrite` sinalizador (implicando Habilitar leitura) em seu registro.

    Os manipuladores de propriedade são abertos para **leitura** (GPS \_ padrão), por padrão, habilite outros leitores, mas negue outros gravadores. Os manipuladores podem optar por habilitar outros gravadores especificando o `EnableShareDenyNone` sinalizador em seu registro. Isso significa que um manipulador pode manipular com êxito uma situação na qual o conteúdo de um arquivo é alterado enquanto o manipulador está lendo o arquivo.

    Para definições de sinalizador, consulte [**GETPROPERTYSTOREFLAGS**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Noções básicas sobre manipuladores de propriedade](./building-property-handlers-properties.md)
</dt> <dt>

[Usando nomes de tipos](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Usando listas de propriedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inicializando manipuladores de propriedade](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Práticas recomendadas e perguntas frequentes do manipulador de propriedades](./prophand-bestprac-faq.md)
</dt> </dl>

 

 

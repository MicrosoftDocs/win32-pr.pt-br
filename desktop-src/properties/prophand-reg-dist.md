---
description: Este artigo explica como registrar e distribuir manipuladores de propriedade para trabalhar com o sistema de propriedades do Windows.
ms.assetid: E6E81E04-9CC1-4df5-9A87-DE0CBD177356
title: Registrando e distribuindo manipuladores de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cffd6169ecbf371e49e27c555f468cdc03e2c3fc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408339"
---
# <a name="registering-and-distributing-property-handlers"></a>Registrando e distribuindo manipuladores de propriedade

Este tópico explica como criar e registrar manipuladores de propriedade para trabalhar com o sistema de propriedades do Windows.

Este tópico é organizado da seguinte forma:

-   [Registrando e distribuindo manipuladores de propriedade](#registering-and-distributing-property-handlers)
-   [Considerações sobre desempenho e confiabilidade para manipuladores de propriedades](#performance-and-reliability-considerations-for-property-handlers)
    -   [Diretrizes para desempenho e confiabilidade](#guidelines-for-performance-and-reliability)
-   [Tópicos relacionados](#related-topics)

## <a name="registering-and-distributing-property-handlers"></a>Registrando e distribuindo manipuladores de propriedade

Depois que o manipulador de propriedades é implementado, ele deve ser registrado e sua extensão de nome de arquivo deve ser associada ao manipulador. O exemplo a seguir usando a extensão .recipe ilustra as entradas necessárias do Registro para fazer isso.

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

Manipuladores de propriedade para um tipo de arquivo específico são normalmente distribuídos com os aplicativos que criam ou manipulam arquivos desse tipo. No entanto, você também deve considerar disponibilizar seus manipuladores de propriedades independentemente desses aplicativos para dar suporte à indexação do tipo de arquivo em cenários de servidor em que os manipuladores de propriedades são usados pelo indexador, mas seus aplicativos que o acompanham não são necessários. Se você criar um pacote de instalação autônomo para o manipulador de propriedades, certifique-se de que ele inclua o seguinte:

-   Os detalhes de registro do manipulador de propriedades especificados no tópico [Registrando e distribuindo manipuladores de propriedade]().
-   Registro para o tipo de arquivo e todos os arquivos de esquema que devem ser instalados, para permitir que os clientes acessem todos os recursos do manipulador de propriedades.

## <a name="performance-and-reliability-considerations-for-property-handlers"></a>Considerações sobre desempenho e confiabilidade para manipuladores de propriedades

Manipuladores de propriedade são invocados para cada arquivo em um computador específico. Normalmente, eles são chamados nas seguintes circunstâncias:

-   Durante a indexação do arquivo. Isso é feito fora do processo, em um processo isolado com direitos restritos.
-   Quando os arquivos são acessados Windows Explorer com a finalidade de ler e escrever valores de propriedade. Isso é feito em processo.

### <a name="guidelines-for-performance-and-reliability"></a>Diretrizes para desempenho e confiabilidade

A qualquer momento, um usuário pode ter dezenas de milhares de arquivos de qualquer tipo específico (incluindo o seu) em seus computadores e pode acessar ou modificar qualquer ou todos esses arquivos a qualquer momento. Como os manipuladores de propriedades são frequentemente invocados para dar suporte a essas operações de acesso e modificação, as características de desempenho e confiabilidade do manipulador de propriedades em ambientes ocupados e altamente simultâneos são de importância crítica.

Tenha em mente as diretrizes a seguir conforme você está desenvolvendo e testando seu manipulador de propriedades.

-   **Enumeração de propriedade**

    Os manipuladores de propriedades devem ter um tempo de resposta muito rápido na enumeração de suas propriedades. Cálculos com uso intensivo de memória de valores de propriedade, pesquisas de rede ou a pesquisa de recursos diferentes do próprio arquivo devem ser evitados para garantir tempos de resposta rápidos.

-   **Escrita de propriedade in-in-place**

    Se possível, ao lidar com arquivos médios ou grandes (várias centenas de KB ou maiores), o formato de arquivo deve ser organizado para que a leitura ou a escrita de valores de propriedade não exigem a leitura de todo o arquivo do disco. Mesmo que o arquivo precise ser procurado, ele não deve ser lido na memória em sua totalidade porque isso sobrecarra o conjunto de trabalho do Windows Explorer ou do indexador Windows Search conforme eles tentam acessar ou indexar esses arquivos. Para obter mais informações, consulte [Inicializando manipuladores de propriedade](./building-property-handlers-property-handlers.md).

    Uma técnica útil para fazer isso é colocar o título do arquivo com espaço extra para que, na próxima vez que um valor da propriedade precisar ser gravado, o valor possa ser gravado no local sem a necessidade de reescrever todo o arquivo. Isso requer a funcionalidade ManualSafeSave. Essa abordagem envolve algum risco extra de que a operação de gravação de arquivo possa ser interrompida enquanto a gravação está em andamento (devido a uma falha do sistema ou perda de energia), mas como os tamanhos de propriedade geralmente são pequenos, a probabilidade dessa interrupção é semelhantemente pequena e os ganhos de desempenho que podem ser obtidos por meio da gravação de propriedade in-loco são considerados significativos o suficiente para justificar esse risco adicional. Mesmo assim, você deve ter cuidado para testar extensivamente sua implementação para garantir que seus arquivos não sejam corrompidos caso uma falha surja no decorrer de uma operação de gravação.

    Por fim, ao implementar a escrita de propriedade in-loco com ManualSafeSave, às vezes, a operação não pode ser executada in-loco e todo o fluxo deve ser reescrito mesmo assim. Para facilitar a reescrita, o fluxo fornecido durante a inicialização do manipulador dá suporte à interface [**IDestinationStreamFactory.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory) A interface **IDestinationStreamFactory** permite que as implementações de manipulador obtenham um fluxo temporário para escrita; quando todas as gravações são concluídas e o método [**IDestinationStreamFactory::GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream) é chamado, esse fluxo é usado para substituir totalmente o fluxo de arquivos original. Quando o fluxo de destino é usado, o fluxo de arquivos original deve ser tratado como somente leitura, porque ele será substituído pelo fluxo de destino depois que o método **IDestinationStreamFactory::GetDestinationStream** tiver sido chamado.

-   **Escolhendo seu modelo de threading COM**

    Para maximizar a eficiência do manipulador de propriedades, você deve especificar que ele usa o modelo de threading COM `Both` . Isso permite o acesso direto de apartments STA (Windows Explorer, por exemplo) e apartments do MTA (agente de transferência de mensagens) (o processo SearchProtocolHost no Windows Search, por exemplo), evitando a sobrecarga de marshaling nesses ambientes. Para obter o benefício completo do modelo de threading, todos os serviços dos quais o manipulador depende também devem ser designados como para evitar marshaling em chamadas para `Both` `Both` esses componentes. Verifique a documentação desses serviços específicos para verificar se eles usam esse modelo de threading.

-   **Concurrency do manipulador de propriedades**

    Os manipuladores de propriedades e a interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) são projetados para acesso serial em vez de simultâneo. Windows Explorer, o indexador Windows Search e todas as outras invocações de manipulador de propriedade da base de código do Windows garantem esse uso. Não deve haver motivo para terceiros usarem um manipulador de propriedades simultaneamente, mas esse comportamento não pode ser garantido. Além disso, embora se espera que o padrão de chamada seja serial, as chamadas podem vir em threads diferentes (por exemplo, quando o objeto está sendo chamado remotamente por meio de COM RPC, como ocorre no indexador). Portanto, as implementações do manipulador de propriedades devem dar suporte a serem chamadas em threads diferentes e, idealmente, não devem sofrer efeitos colaterais quando chamadas simultaneamente. Como o padrão de chamada pretendido é serial, uma implementação trivial usando uma seção crítica deve ser suficiente para atender a esses requisitos na maioria dos casos. É aceitável evitar o bloqueio em chamadas simultâneas usando a [**função TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) para detectar e falhar chamadas simultâneas.

-   **Concurreência de arquivo**

    Manipuladores de propriedades geralmente são usados em cenários em que vários aplicativos acessam um arquivo simultaneamente. Portanto, o manipulador e os aplicativos precisam gerenciar a simultrreidade especificando os modos de compartilhamento apropriados ao abrir o arquivo. Eles também precisam estar cientes do acesso que os outros aplicativos especificam e para gerenciar casos em que o acesso não é permitido. É melhor que todos os consumidores especifiquem modos de compartilhamento de dados para permitir que outras pessoas acessem o arquivo simultaneamente, mas, ao fazer isso, os problemas de consistência precisam ser gerenciados. As decisões sobre os modos de compartilhamento mais apropriados a serem usados precisam ser tomadas no contexto da comunidade de aplicativos que acessam o arquivo.

    Os sistemas de arquivos permitem que os aplicativos abram arquivos de uma maneira que dê a eles controle sobre se e como outros aplicativos podem abrir o arquivo. Os modos de compartilhamento permitem acesso de leitura, gravação e exclusão. O sistema de propriedades dá suporte a um subconjunto desses modos de compartilhamento, descrito na tabela a seguir.

    

    | Modo de acesso                     | Modo de compartilhamento                             |
    |---------------------------------|------------------------------------------|
    | Gravar                           | Negar outros leitores e autores           |
    | Gravação (EnableShareDenyWrite)    | Habilitar outros leitores, negar outros autores |
    | Somente leitura (padrão)             | Habilitar outros leitores, negar outros autores |
    | Somente leitura (EnableShareDenyNone) | Habilitar outros leitores e autores         |

    

     

    Manipuladores de propriedades abertos **para gravação** (GPS \_ READWRITE) negarão outros leitores e autores. Os manipuladores podem optar por um comportamento que habilita os leitores especificando o sinalizador (implicando habilitar `EnableShareDenyWrite` Leitura) em seu registro.

    Manipuladores de propriedades abertos para **leitura** (GPS \_ DEFAULT), por padrão habilitam outros leitores, mas negam outros autores. Os manipuladores podem optar por habilenciar outros autores especificando o `EnableShareDenyNone` sinalizador em seu registro. Isso significa que um manipulador pode lidar com uma situação na qual o conteúdo de um arquivo muda enquanto o manipulador está lendo o arquivo.

    Para definições de sinalizador, [**consulte GETPROPERTYSTOREFLAGS**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Noções básicas sobre manipuladores de propriedade](./building-property-handlers-properties.md)
</dt> <dt>

[Usando nomes de tipo](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Usando listas de propriedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inicializando manipuladores de propriedades](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Práticas recomendadas e perguntas frequentes do manipulador de propriedades](./prophand-bestprac-faq.md)
</dt> </dl>

 

 

---
title: Assinatura de raiz versão 1,1
description: A finalidade da assinatura de raiz versão 1,1 é permitir que os aplicativos indiquem drivers quando os descritores em um heap de descritor não forem alterados ou se o ponto dos descritores de dados não forem alterados.
ms.assetid: 8FE42C1C-7F1D-4E70-A7EE-D5EC67237327
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d0a107b4186f164e60a6225f55c5ba3f4f06b2
ms.sourcegitcommit: f5a319899176e2df564bdb4d9eaffc32140452a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2020
ms.locfileid: "104548276"
---
# <a name="root-signature-version-11"></a>Assinatura de raiz versão 1,1

A finalidade da assinatura de raiz versão 1,1 é permitir que os aplicativos indiquem drivers quando os descritores em um heap de descritor não forem alterados ou se o ponto dos descritores de dados não forem alterados. Isso permite que a opção de drivers crie otimizações que podem ser possíveis de saber que um descritor ou a memória apontada por ele é estático por um período de tempo.

-   [Visão geral](#overview)
-   [Sinalizadores estáticos e voláteis](#static-and-volatile-flags)
    -   [DESCRITOres \_ voláteis](#descriptors_volatile)
    -   [DADOS \_ voláteis](#data_volatile)
    -   [DADOS \_ estáticos \_ ao serem \_ definidos \_ em \_ execução](#data_static_while_set_at_execute)
    -   [DADOS \_ estáticos](#data_static)
    -   [Combinando sinalizadores](#combining-flags)
    -   [Resumo do sinalizador](#flag-summary)
-   [Resumo da API da versão 1,1](#version-11-api-summary)
    -   [Enumerações](#enums)
    -   [Estruturas](#helper-structures)
    -   [Funções](#functions)
    -   [Métodos](#methods)
    -   [Estruturas auxiliares](#helper-structures)
-   [Consequências de violar sinalizadores qualidade estáticos](#consequences-of-violating-static-ness-flags)
-   [Gerenciamento de versões](#version-management)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

A assinatura de raiz versão 1,0 permite que o conteúdo de heaps de descritor e a memória que eles apontam para serem alterados livremente pelos aplicativos sempre que as listas de comandos/pacotes que os referenciam são potencialmente em trânsito na GPU. No entanto, com muita frequência, os aplicativos não precisam realmente da flexibilidade para alterar os descritores ou a memória depois que os comandos que fazem referência a eles foram registrados.

Normalmente, os aplicativos são capazes de:

-   Configure descritores (e possível a memória para a qual apontam) antes de associar as tabelas de descrição ou os descritores de raiz em uma lista de comandos ou um pacote.
-   Certifique-se de que esses descritores não serão alterados até que a lista de comandos/Bundles de fazer referência a eles tenha concluído a execução pela última vez.
-   Verifique se os dados aos quais os descritores apontam não são alterados para a mesma duração total.

Como alternativa, um aplicativo só pode ser capaz de honrar que os dados não são alterados por uma duração menor no tempo. Em particular, os dados podem ser estáticos para a janela no tempo durante a execução da lista de comandos que uma associação de parâmetro raiz (tabela de descritores ou descritor raiz) aponta para os dados no momento. Em outras palavras, um aplicativo pode desejar executar a execução na linha do tempo da GPU que atualiza alguns dados entre os períodos de tempo em que são definidos por meio de um parâmetro raiz, sabendo que, quando ele for definido, será estático.

Se descritores ou os descritores de dados apontarem para, não serão alterados, os drivers de otimizações específicos podem ser específicos do fornecedor de hardware e, de forma importante, não alteram o comportamento, o que não é possível melhorar o desempenho. A preservação da maior parte do conhecimento sobre a intenção do aplicativo, como possível, não sobrecarrega os aplicativos.

Uma otimização é que muitos drivers podem produzir acessos de memória mais eficientes por sombreadores, caso saibam as promessas que um aplicativo pode tomar sobre o qualidade estático de descritores e dados. Por exemplo, os drivers podem remover um nível de indireção para acessar um descritor em um heap convertendo-o em um descritor raiz se o hardware específico não for sensível ao tamanho do argumento raiz.

A tarefa adicional para o desenvolvedor usar a versão 1,1 é tornar as promessas sobre volatilidade e qualidade de dados sempre que possível, para que os drivers possam fazer as otimizações que fazem sentido. Os desenvolvedores não precisam fazer nenhuma promessa sobre qualidade estático.

A assinatura de raiz versão 1,0 continua a funcionar inalterada, embora os aplicativos que recompilam assinaturas raiz tenham como padrão a assinatura raiz 1,1 agora (com uma opção para forçar a versão 1,0, se desejado).

## <a name="static-and-volatile-flags"></a>Sinalizadores estáticos e voláteis

Os sinalizadores a seguir fazem parte da assinatura raiz para permitir que os drivers escolham uma estratégia de como lidar melhor com os argumentos raiz individuais quando eles são definidos e também incorporar as mesmas suposições aos objetos de estado do pipeline (PSOs) quando eles são compilados originalmente – já que a assinatura raiz faz parte de um PSO.

Os sinalizadores a seguir são definidos pelo aplicativo e aplicam-se a descritores ou dados.

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_FLAGS
{
    D3D12_DESCRIPTOR_RANGE_FLAG_NONE    = 0,
    D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE    = 0x1,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_VOLATILE   = 0x2,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE    = 0x4,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC = 0x8
} D3D12_DESCRIPTOR_RANGE_FLAGS;

typedef enum D3D12_ROOT_DESCRIPTOR_FLAGS
{
    D3D12_ROOT_DESCRIPTOR_FLAG_NONE = 0,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_VOLATILE    = 0x2,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE = 0x4,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC  = 0x8
} D3D12_ROOT_DESCRIPTOR_FLAGS;
```

### <a name="descriptors_volatile"></a>DESCRITOres \_ voláteis

Com esse sinalizador definido, os descritores em um heap de descritores apontados por uma tabela de descritor raiz podem ser alterados pelo aplicativo a qualquer momento, exceto quando a lista de comandos/pacotes que associam a tabela de descritores foram enviados e não concluíram a execução. Por exemplo, gravar uma lista de comandos e, subsequentemente, alterar os descritores em um heap de descritores ao qual se refere *antes* de enviar a lista de comandos para execução é válido. Esse é o único comportamento com suporte da assinatura raiz versão 1,0.

Se o sinalizador volátil dos DESCRITOres \_ *não* for definido, os descritores serão estáticos. Não há nenhum sinalizador para esse modo. Os descritores estáticos significam que os descritores em um heap de descritores apontados por uma tabela de descrição de raiz foram inicializados pela hora em que a tabela de descritores é definida em uma lista de comandos/pacote (durante a gravação) e os descritores não podem ser alterados até que a lista de comandos/pacote tenha terminado a execução pela última vez. *Para a assinatura raiz versão 1,1, os descritores estáticos são a suposição padrão* e o aplicativo precisa especificar o sinalizador volátil dos descritores \_ quando necessário.

Para os pacotes que usam tabelas de descritores com descripdores estáticos, os descritores precisam estar prontos começando no momento em que o pacote é registrado (ao contrário de quando o pacote é chamado) e não é alterado até que a execução do pacote seja concluída pela última vez. As tabelas de descritores que apontam para descritores estáticos precisam ser definidas durante a gravação do pacote e não herdadas no grupo. É válido para uma lista de comandos usar uma tabela de descritores com descripdores estáticos que foram definidos em um pacote e retornados de volta à lista de comandos.

Quando os descritores são estáticos, há outra alteração no comportamento que exige que o sinalizador volátil de DESCRITOres \_ seja definido. Acessos fora dos limites a quaisquer exibições de buffer (em oposição às exibições Texture1D/2D/3D/Cube) são inválidos e produzem resultados indefinidos, incluindo possível redefinição de dispositivo, em vez de retornar valores padrão para leituras ou descartar gravações. A finalidade de remover a capacidade dos aplicativos de depender do hardware fora dos limites de verificação de acesso é permitir que os drivers escolham promover acessos de descritor estáticos a acessos de descritor de raiz se considerarem isso mais eficiente. Os descritores raiz não dão suporte a nenhuma verificação fora dos limites.

Se os aplicativos dependerem do comportamento de acesso à memória fora dos limites ao acessar os descritores, eles precisarão marcar os intervalos de descritores que acessam esses descripdores como DESCRITOres \_ voláteis.

### <a name="data_volatile"></a>DADOS \_ voláteis

Com esse sinalizador definido, os dados apontados por descritores podem ser alterados pela CPU a qualquer momento, exceto enquanto os pacotes/lista de comandos que associam a tabela de descritor foram enviados e não concluíram a execução. Esse é o único comportamento com suporte da assinatura raiz versão 1,0.

O sinalizador está disponível nos sinalizadores de intervalo de descritores e no descritor de raiz.

### <a name="data_static_while_set_at_execute"></a>DADOS \_ estáticos \_ ao serem \_ definidos \_ em \_ execução

Com esse sinalizador definido, os dados apontados por descritores não podem mudar a partir de quando o descritor raiz subjacente ou a tabela de descritor é definido em uma lista de comandos/pacote durante a execução na linha do tempo da GPU e terminando quando o desenho/despacho subsequentes não fará mais referência aos dados.

Antes de um descritor raiz ou uma tabela de descritores ter sido definida na GPU, esses dados *podem* ser alterados mesmo pela mesma lista de comandos/pacote. Os dados também podem ser alterados enquanto um descritor raiz ou uma tabela de descritores apontando para ele ainda estiver definido na lista de comandos/pacote, desde que os empates/expedimentos que fazem referência a ele tenham sido concluídos. No entanto, isso requer que a tabela de descritores seja reassociada à lista de comandos novamente antes da próxima vez que a tabela de descritor ou descritor raiz for desreferenciada. Isso permite que o driver saiba que os dados apontados por um descritor raiz ou uma tabela de descritores foram alterados.

A diferença essencial entre os dados \_ estáticos \_ enquanto \_ definido \_ em \_ Execute e dados \_ voláteis é com dados \_ voláteis um driver não pode informar se as cópias de dados em uma lista de comandos alteraram os dados apontados por um descritor, sem fazer acompanhamento de estado extra. Portanto, se, por exemplo, um driver puder inserir qualquer tipo de comando de pré-busca de dados em sua lista de comandos (para tornar o sombreador o acesso a dados conhecidos mais eficiente, por exemplo), \_ os dados estáticos \_ enquanto \_ definidos \_ em \_ Execute permitem que o driver saiba que ele só precisa executar a pré-busca de dados no momento em que ele é definido por meio de [**SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable), [**SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable) ou um dos métodos para definir a exibição de buffer constante, a exibição de recursos do sombreador ou a exibição de acesso não ordenado.

Para os pacotes, a promessa de que os dados são estáticos enquanto definido em executar aplica-se exclusivamente a cada execução do pacote.

O sinalizador está disponível nos sinalizadores de intervalo de descritores e no descritor de raiz.

### <a name="data_static"></a>DADOS \_ estáticos

Se esse sinalizador for definido, os dados apontados por descritores serão inicializados no momento em que uma tabela de descritor ou descritor de raiz que faz referência à memória foi definida em uma lista de comandos/pacote durante a gravação, e os dados não poderão ser alterados até que a lista de comandos/pacote tenha terminado a execução pela última vez.

Para os pacotes, a duração estática começa no descritor raiz ou na configuração da tabela de descritores durante a gravação do pacote, em oposição à gravação de uma lista de comandos de chamada. Além disso, uma tabela de descritores apontando para dados estáticos deve ser definida no grupo e não herdada. É válido para uma lista de comandos usar uma tabela de descritores apontando para dados estáticos que foram definidos em um pacote e retornados de volta para a lista de comandos.

O sinalizador está disponível nos sinalizadores de intervalo de descritores e no descritor de raiz.

### <a name="combining-flags"></a>Combinando sinalizadores

No máximo um dos sinalizadores de dados pode ser especificado por vez, exceto por intervalos de descritores de amostras que não dão suporte a sinalizadores de dados, já que os exemplos não apontam para dados.

A ausência de qualquer sinalizador de dados para intervalos de descritor SRV e CBV significa um padrão de dados \_ estáticos \_ enquanto \_ definido \_ no \_ comportamento de execução é assumido. O motivo pelo qual esse padrão é escolhido, em vez de dados \_ estáticos, é que os dados \_ estáticos, \_ enquanto \_ definidos \_ em \_ Execute, têm muito mais probabilidade de ser um padrão seguro para a maioria dos casos, enquanto ainda geram uma oportunidade de otimização melhor do que o padrão para dados \_ voláteis.

A ausência de sinalizadores de dados para intervalos de descritores UAV significa que um padrão de \_ comportamento volátil de dados é assumido, dado normalmente UAVs são gravados em.

Os DESCRITOres \_ voláteis *não podem* ser combinados com dados \_ estáticos, mas *podem* ser combinados com os outros sinalizadores de dados. O motivo pelo qual os DESCRITOres \_ voláteis podem ser combinados com os dados \_ estáticos \_ enquanto \_ definido \_ em \_ execução é que os descritores voláteis ainda exigem que os descritores estejam prontos durante a execução da lista de comandos/pacote, e os dados \_ estáticos, \_ enquanto \_ definidos \_ em \_ Execute, sejam apenas prometedos sobre o qualidade estático dentro de um subconjunto da execução da lista de comandos/pacote.

### <a name="flag-summary"></a>Resumo do sinalizador

As tabelas a seguir resumem as combinações de sinalizador que podem ser empregadas.



|                                                                |                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Configurações de \_ \_ sinalizadores de intervalo do descritor D3D12 válidas \_**             | **Descrição**                                                                                                                                                                                                                                                                                                                                      |
| Nenhum sinalizador definido                                                   | Os descritores são estáticos (o padrão). Suposições padrão para dados: para SRV/CBV: dados \_ estáticos \_ enquanto \_ definidos \_ em \_ Execute e para UAV: data \_ volatile. Esses padrões para SRV/CBV se ajustarão com segurança aos padrões de uso para a maioria das assinaturas raiz.                                                                                              |
| DADOS \_ estáticos                                                   | Os dois descritores e os dados são estáticos. Isso maximiza o potencial para otimização de driver.                                                                                                                                                                                                                                                          |
| DADOS \_ voláteis                                                 | Os descritores são estáticos e os dados são voláteis.                                                                                                                                                                                                                                                                                                     |
| DADOS \_ estáticos \_ ao serem \_ definidos \_ em \_ execução                          | Os descritores são estáticos e os dados são estáticos enquanto definidos em execute.                                                                                                                                                                                                                                                                                      |
| DESCRITOres \_ voláteis                                          | Os descritores são voláteis e as suposições padrão são feitas sobre os dados: para SRV/CBV: os dados são \_ estáticos \_ enquanto \_ definidos \_ em \_ Execute e para UAV: data \_ volatile.                                                                                                                                                                                              |
| dados voláteis de DESCRITOres voláteis \_ \| \_                        | Os dois descritores e os dados são voláteis, equivalentes à assinatura raiz 1,0.                                                                                                                                                                                                                                                                            |
| \_ \| dados voláteis de descritores \_ estáticos \_ enquanto \_ definidos \_ em \_ execução | Os descritores são voláteis, mas observe que ainda não permite que eles sejam alterados durante a execução da lista de comandos. Portanto, é válido combinar a declaração adicional de que os dados são estáticos ao serem definidos por meio da tabela do descritor raiz durante a execução – os descritores subjacentes são efetivamente estáticos por mais tempo do que os dados estão sendo prometidos para serem estáticos. |



 



|                                                   |                                                                                                                                                                                                                   |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Configurações de \_ \_ sinalizadores do descritor raiz D3D12 válido \_** | **Descrição**                                                                                                                                                                                                   |
| Nenhum sinalizador definido                                      | Suposições padrão para dados: para SRV/CBV: dados \_ estáticos \_ enquanto \_ definidos \_ em \_ Execute e para UAV: data \_ volatile. Esses padrões para SRV/CBV se ajustarão com segurança aos padrões de uso para a maioria das assinaturas raiz. |
| DADOS \_ estáticos                                      | Os dados são estáticos, o melhor potencial para a otimização do driver.                                                                                                                                                       |
| DADOS \_ estáticos \_ ao serem \_ definidos \_ em \_ execução             | Os dados são estáticos enquanto definidos em execute.                                                                                                                                                                              |
| DADOS \_ voláteis                                    | Equivalente à assinatura raiz 1,0.                                                                                                                                                                                 |



 

## <a name="version-11-api-summary"></a>Resumo da API da versão 1,1

As seguintes chamadas à API habilitam a versão 1,1.

### <a name="enums"></a>Enumerações

Essas enumerações contêm os sinalizadores de chave para especificar o descritor e os dados volatilidade.

-   [**D3D \_ \_ \_ Versão da assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version) : IDs de versão.
-   [**D3D12 \_ \_ \_ Sinalizadores de intervalo de descritores**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) : um intervalo de sinalizadores que determinam se os dados ou descritores são voláteis ou estáticos.
-   [**D3D12 \_ \_ \_ Sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) : um intervalo semelhante de sinalizadores para [**\_ \_ \_ sinalizadores de intervalo de descritor D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags), exceto que somente os sinalizadores de dados se aplicam a descritores de raiz.

### <a name="structures"></a>Estruturas

As estruturas atualizadas (da versão 1,0) contêm referências aos sinalizadores volatilidade/static.

-   [**D3D12 \_ \_ \_ \_ Assinatura raiz dos dados do recurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature) : passe essa estrutura para [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) para verificar o suporte à assinatura de raiz versão 1,1.
-   [**D3D12 \_ Assinatura de \_ raiz com versão \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) : pode conter qualquer versão de uma descrição de assinatura raiz e foi projetada para ser usada com as funções de serialização/desserialização listadas abaixo.
-   Essas estruturas são equivalentes àquelas usadas na versão 1,0, com a adição de novos campos flags para os intervalos de descritores e os descritores raiz:

    -   [**D3D12 \_ de \_ assinatura raiz \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1)
    -   [**D3D12 \_ descritor \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
    -   [**D3D12 \_ do \_ descritor raiz \_ Table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
    -   [**D3D12 \_ raiz \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
    -   [**D3D12 \_ raiz \_ parâmetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

### <a name="functions"></a>Funções

Os métodos listados aqui substituem as funções [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) e [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) originais, pois elas são projetadas para funcionar em qualquer versão da assinatura raiz. O formulário serializado é o que é passado para a API [**CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) . Se um sombreador tiver sido criado com uma assinatura raiz nele, o sombreador compilado conterá uma assinatura de raiz serializada já existente.

-   [**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) : se um aplicativo gerar um procedimento de acordo com a estrutura de dados da [**\_ \_ \_ assinatura raiz do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) , ele deverá fazer o formulário serializado usando essa função.
-   [**D3D12CreateVersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) : gera uma interface que pode retornar a estrutura de dados desserializada, por meio de [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc).

### <a name="methods"></a>Métodos

A interface [**ID3D12VersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) é criada para desserializar a estrutura de dados de assinatura raiz.

-   [**GetRootSignatureDescAtVersion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getrootsignaturedescatversion) : converte estruturas de descrição de assinatura raiz para uma versão solicitada.
-   [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc) : retorna um ponteiro para uma [**estrutura \_ \_ \_ \_ desc de assinatura raiz D3D12 com controle de versão**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

### <a name="helper-structures"></a>Estruturas auxiliares

Foram adicionadas estruturas auxiliares para auxiliar na inicialização de algumas das estruturas da versão 1,1.

-   CD3DX12 \_ descritor \_ RANGE1
-   CD3DX12 \_ raiz \_ parâmetro1
-   \_SAMPLER1 CD3DX12 static \_
-   \_Desc. de \_ \_ assinatura raiz \_ CD3DX12 com versão

Consulte [estruturas auxiliares e funções para D3D12](helper-structures-and-functions-for-d3d12.md).

## <a name="consequences-of-violating-static-ness-flags"></a>Consequências de violar sinalizadores qualidade estáticos

Os sinalizadores de descritor e de dados descritos acima (bem como os padrões implícitos pela ausência de sinalizadores específicos) definem uma promessa pelo aplicativo para o driver sobre como ele se comportará. Se um aplicativo violar a promessa, esse comportamento é inválido: os resultados são indefinidos e podem ser diferentes em diferentes drivers e hardware.

A camada de depuração tem opções para validar se os aplicativos honram suas promessas, incluindo as promessas padrão que acompanham o uso da versão 1,1 da assinatura raiz sem definir nenhum sinalizador.

## <a name="version-management"></a>Gerenciamento de versões

Ao compilar assinaturas raiz anexadas a sombreadores, os compiladores HLSL mais recentes terão como padrão a compilação da assinatura raiz na versão 1,1, enquanto os compiladores de HLSL antigos só dão suporte a 1,0. Observe que 1,1 assinaturas raiz não funcionarão no sistema operacional que não dão suporte à assinatura raiz 1,1.

A versão de assinatura raiz compilada com um sombreador pode ser forçada para uma versão específica usando `/force_rootsig_ver <version>` . A força da versão terá sucesso se o compilador puder preservar o comportamento da assinatura raiz que está sendo compilada na versão forçada, por exemplo, descartando os sinalizadores sem suporte na assinatura raiz que servem apenas para fins de otimização, mas que não afetam o comportamento.

Dessa forma, um aplicativo pode, por exemplo, compilar uma assinatura raiz 1,1 para 1,0 e 1,1 ao compilar o aplicativo e selecionar a versão apropriada em tempo de execução, dependendo do nível de suporte do sistema operacional. No entanto, seria a maior parte do espaço eficiente para um aplicativo compilar assinaturas raiz individualmente (especialmente se várias versões forem necessárias), separadamente dos sombreadores. Mesmo que os sombreadores não sejam inicialmente compilados com uma assinatura raiz anexada, o benefício da validação do compilador da compatibilidade de assinatura raiz com um sombreador pode ser preservado usando a `/verifyrootsignature` opção do compilador. Posteriormente em tempo de execução, PSOs pode ser criado usando sombreadores que não têm assinaturas raiz neles enquanto passa a assinatura raiz desejada (talvez a versão apropriada com suporte do sistema operacional) como um parâmetro separado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma assinatura raiz](creating-a-root-signature.md)
</dt> <dt>

[Assinaturas raiz](root-signatures.md)
</dt> <dt>

[Especificando assinaturas raiz em HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 





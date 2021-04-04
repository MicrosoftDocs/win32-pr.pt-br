---
title: Latência de rede e taxa de transferência
description: Latência de rede e taxa de transferência com RPC (chamada de procedimento remoto).
ms.assetid: 8285fd73-eb54-4c06-b01a-1bffafb7e675
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c51c4db75b904ac5feae8c4a1cc5965fc2b06e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160300"
---
# <a name="network-latency-and-throughput"></a>Latência de rede e taxa de transferência

Três problemas importantes estão relacionados ao uso ideal da rede:

-   Latência da rede
-   Saturação de rede
-   Implicações de processamento de pacotes

Esta seção apresenta uma tarefa de programação que requer o uso de RPC e, em seguida, projeta duas soluções: uma mal gravada e uma bem gravada. As duas soluções são então fiscalizadas e seu impacto no desempenho da rede é discutido.

Antes de discutir as duas soluções, as próximas seções discutem e esclarecem os problemas de desempenho relacionados à rede.

## <a name="network-latency"></a>Latência de rede

A largura de banda de rede e a latência de rede são termos separados. Redes com alta largura de banda não garantem baixa latência. Por exemplo, um caminho de rede atravessando um link satélite geralmente tem alta latência, embora a taxa de transferência seja muito alta. Não é incomum uma viagem de ida e volta da rede atravessando um link satélite para ter cinco ou mais segundos de latência. A implicação desse atraso é: um aplicativo projetado para enviar uma solicitação, aguardar uma resposta, enviar outra solicitação, aguardar outra resposta e assim por diante, aguardará pelo menos cinco segundos para cada troca de pacotes, independentemente da velocidade do servidor. Apesar da velocidade crescente dos computadores, as transmissões por satélite e a mídia de rede são baseadas na velocidade da luz, o que geralmente permanece constante. Dessa forma, as melhorias na latência para redes satélite existentes provavelmente não ocorrerão.

## <a name="network-saturation"></a>Saturação de rede

Alguma saturação ocorre em muitas redes. As redes mais fáceis de saturar são links de modem lentos, como modems analógicos padrão de 56K. No entanto, os links Ethernet com muitos computadores em um único segmento também podem ser saturados. O mesmo se aplica a redes de longa distância, com uma baixa largura de banda ou um link sobrecarregado de outra forma, como um roteador ou um comutador que possa lidar com uma quantidade limitada de tráfego. Nesses casos, se a rede enviar mais pacotes do que o link mais fraco pode manipular, ele descartará os pacotes. Para evitar o congestionamento, a pilha TCP do Windows é dimensionada de volta quando pacotes descartados são detectados, o que pode resultar em atrasos significativos.

## <a name="packet-processing-implications"></a>Implicações de processamento de pacotes

Quando os programas são desenvolvidos para ambientes de nível superior, como RPC, COM e até mesmo Windows Sockets, os desenvolvedores tendem a se esquecer da quantidade de trabalho que ocorre nos bastidores de cada pacote enviado ou recebido. Quando um pacote chega da rede, uma interrupção da placa de rede é atendida pelo computador. Em seguida, uma DPC (chamada de procedimento deferida) é enfileirada e deve fazer o caminho pelos drivers. Se qualquer forma de segurança for usada, o pacote poderá ter que ser descriptografado ou o hash criptográfico verificado. Várias verificações de validade também devem ser executadas em cada Estado. Somente o pacote chega no destino final: o código do servidor. O envio de muitas partes pequenas de resultados de dados na sobrecarga de processamento de pacotes para cada pequena parte dos dados. O envio de uma grande parte dos dados tende a consumir significativamente menos tempo de CPU em todo o sistema, embora o custo de execução de muitas partes pequenas em comparação com uma grande parte seja o mesmo para o aplicativo de servidor.

## <a name="example-1-a-poorly-designed-rpc-server"></a>Exemplo 1: um servidor RPC mal projetado

Imagine um aplicativo que deve acessar arquivos remotos e a tarefa em questão é criar uma interface RPC para manipular o arquivo remoto. A solução mais simples é espelhar as rotinas de arquivo do estúdio para arquivos locais. Fazer isso pode resultar em uma interface bem limpa e familiar. Este é um arquivo. idl abreviado:

``` syntax
typedef [context_handle] void *remote_file;
... .
interface remote_file
{
    remote_file remote_fopen(file_name);
    void remote_fclose(remote_file ...);
    size_t remote_fread(void *, size_t, size_t, remote_file ...);
    size_t remote_fwrite(const void *, size_t, size_t, remote_file ...);
    size_t remote_fseek(remote_file ..., long, int);
}
```

Isso parece elegante o bastante, mas, na verdade, essa é uma receita que é cumprida por um desastre de desempenho. Ao contrário da opinião popular, a chamada de procedimento remoto não é simplesmente uma chamada de procedimento local com um fio entre o chamador e o receptor.

Para ver como essa receita grava o desempenho, considere um arquivo de 2K, onde 20 bytes são lidos desde o início e, em seguida, 20 bytes do final e veja como isso é executado. No lado do cliente, as seguintes chamadas são feitas (muitos caminhos de código são omitidos para fins de brevidade):

``` syntax
rfp = remote_fopen("c:\\sample.txt");
remote_read(...);
remote_fseek(...);
remote_read(...);
remote_fclose(rfp);
```

Agora imagine que o servidor esteja separado do cliente por um link de satélite com um tempo de ida e volta de cinco segundos. Cada uma dessas chamadas deve aguardar uma resposta antes que possa continuar, o que significa um mínimo absoluto para executar essa sequência de 25 segundos. Considerando que estamos recuperando apenas 40 bytes, isso é outrageously o desempenho lento. Os clientes desse aplicativo seriam assombrosa.

Agora imagine que a rede está saturada, pois a capacidade de um roteador em algum lugar no caminho de rede é sobrecarregada. Esse design força o roteador a lidar com pelo menos 10 pacotes se não tivermos segurança (um para cada solicitação e um para cada resposta). Isso também não é bom.

Esse design também força o servidor a receber cinco pacotes e enviar cinco pacotes. Novamente, não é uma implementação muito boa.

## <a name="example-2-a-better-designed-rpc-server"></a>Exemplo 2: um servidor RPC melhor projetado

Vamos reprojetar a interface discutida no exemplo 1 e ver se podemos melhorar. É importante observar que tornar esse servidor realmente bom requer conhecimento do padrão de uso para os arquivos fornecidos: tal conhecimento não é assumido para este exemplo. Portanto, esse é um servidor RPC melhor projetado, mas não um servidor RPC com design ideal.

A ideia neste exemplo é recolher o máximo possível de operações remotas em uma operação. A primeira tentativa é a seguinte:

``` syntax
typedef [context_handle] void *remote_file;
typedef struct
{
    long position;
    int origin;
} remote_seek_instruction;
... .
interface remote_file
{
    remote_fread(file_name, void *, size_t, size_t, [in, out] remote_file ..., BOOL CloseWhenDone, remote_seek_instruction *...);
    size_t remote_fwrite(file_name, const void *, size_t, size_t, [in, out] remote_file ..., BOOL CloseWhenDone, remote_seek_instruction *...);
}
```

Este exemplo recolhe todas as operações para uma leitura e gravação, o que permite uma abertura opcional na mesma operação, bem como um fechamento e uma busca opcionais.

Essa mesma sequência de operação, quando escrita em formato abreviado, tem a seguinte aparência:

``` syntax
remote_read("c:\\sample.txt", ..., &rfp, FALSE, NULL);
remote_read(NULL, ..., &rfp, TRUE, seek_to_20_bytes_before_end);
```

Ao considerar o servidor RPC melhor projetado, na segunda chamada, o servidor verifica se o *\_ nome do arquivo* é **nulo** e usa o arquivo aberto armazenado na RFP. Em seguida, ele vê que há instruções de busca e posicionará o ponteiro de arquivo 20 bytes antes do final antes de lê-lo. Quando terminar, ele reconhecerá que o sinalizador **CloseWhenDone** está definido como **true** e fechará o arquivo e fechará a RFP.

Na rede de alta latência, essa versão melhor leva 10 segundos para ser concluída (2,5 vezes mais rápido) e requer o processamento de apenas quatro pacotes; dois recebimentos do servidor e dois envios do servidor. O *IFS* extra e o desempacotamento de desempenho do servidor são insignificantes em comparação com todo o resto.

Se a ordenação causal for especificada corretamente, a interface poderá até mesmo se tornar assíncrona e as duas chamadas poderão ser enviadas em paralelo. Quando a ordenação causal é usada, as chamadas ainda são expedidas na ordem, o que significa que, na rede de alta latência, apenas um atraso de cinco segundos é disparado, embora o número de pacotes enviados e recebidos seja o mesmo.

Podemos recolher isso ainda mais criando um método que usa uma matriz de estruturas, cada membro da matriz que descreve uma operação de arquivo específica; uma variação remota de dispersão/coleta de e/s. A abordagem paga desde que o resultado de cada operação não exija processamento adicional no cliente; em outras palavras, o aplicativo vai ler os 20 bytes no final, independentemente da leitura dos primeiros 20 bytes.

No entanto, se algum processamento precisar ser executado nos primeiros 20 bytes depois de lê-los para determinar a próxima operação, recolher tudo em uma única operação não funcionará (pelo menos não em todos os casos). A elegância do RPC é que um aplicativo pode ter ambos os métodos na interface e chamar qualquer método, dependendo da necessidade.

Em geral, quando a rede está envolvida, é melhor combinar quantas chamadas forem possíveis para uma única chamada. Se um aplicativo tiver duas atividades independentes, use operações assíncronas e permita que elas sejam executadas em paralelo. Essencialmente, mantenha o pipeline cheio.

 

 





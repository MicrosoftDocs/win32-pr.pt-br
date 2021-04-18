---
title: Nova API permite que os aplicativos enviem dicas de "corte e desmapeamento" para mídia de armazenamento
description: Nova API permite que os aplicativos enviem \ 0034; APARAr e desmapear \ 0034; Dicas para mídia de armazenamento
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e043c1188bda790b4ed151e8a79e1f7b4c6f0f9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "105797542"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a>Nova API permite que os aplicativos enviem dicas de "corte e desmapeamento" para mídia de armazenamento

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

As dicas de corte notificam a unidade de que determinados setores que foram alocados anteriormente não são mais necessários para o aplicativo e podem ser limpos. Normalmente, isso é usado quando um aplicativo faz alocações de espaço grandes por meio de um arquivo e, em seguida, gerencia automaticamente as alocações para o arquivo (por exemplo, arquivos de disco rígido virtual).

**O que é TRIM?**

Os SSDs (unidades de estado sólido) geralmente são dispositivos flash com base em memória em bloco. Isso significa que, quando os dados são gravados no SSD, eles não podem ser substituídos em lugar algum e devem ser gravados em outro lugar até que o bloco possa ser coletado pelo lixo. Como o SSD não tem nenhum mecanismo interno para determinar se determinados blocos foram removidos e outros são necessários. A única vez em que o SSD pode marcar um setor "sujo" é quando ele é sobrescrito. Em outros casos, como quando um arquivo é excluído, o SSD retém esses setores porque a exclusão é executada apenas como uma alteração de MFT (tabela de arquivos mestre) e não como uma operação para todos os setores do arquivo. No Windows 7, apresentamos uma maneira padrão de se comunicar com SSDs sobre setores que não são mais necessários. Esse comando é definido na [especificação T13](https://www.t13.org/Standards/Default.aspx?DocumentType=3) como o comando Trim; O NTFS envia o comando TRIM para algumas operações internas normais, como "DeleteFile".

**Outros usos de TRIM no mundo de armazenamento**

Como SSDs, redes de área de armazenamento (SANs) e as novas implementações de espaços de software de recurso do Windows 8 consomem dicas de comando de corte para gerenciar seus espaços em ambientes com provisionamento dinâmico. Os espaços de software e SANs alocam regiões de armazenamento em tamanhos maiores que setores ou clusters (em qualquer lugar, de 1 MB a 1GB). Quando eles recebem dicas de corte para seu tamanho de alocação (ou maior que o tamanho de alocação), o SAN/SSD pode desalocar uma região para liberar espaço para outros arquivos. Normalmente, eles passam por todas as dicas de corte para a mídia subjacente (SSD ou HDD) para que possam consumir o espaço liberado conforme apropriado. Normalmente, eles não movem dados para regiões desalocadas, nem controlam áreas de corte em regiões desalocadas (quando a região está vazia).

SANs com provisionamento dinâmico usam as dicas de corte que são passadas a elas para ajudar a reduzir o espaço geral do armazenamento físico, reduzindo assim o custo. A [especificação de SCSI T10](https://www.t10.org) define o comando ' remapeamento ' (semelhante ao comando Trim); aqui, o comando é aplicável a todos os tipos de armazenamento, incluindo HDDs, SSDs e outros. O comando de desmapeamento ajuda a remover blocos físicos da alocação de SAN.

## <a name="how-to-use-the-new-api"></a>Como usar a nova API


```
#define FSCTL_FILE_LEVEL_TRIM CTL_CODE(FILE_DEVICE_FILE_SYSTEM, 130, METHOD_BUFFERED, FILE_WRITE_DATA)

Where 
typedef struct _EXTENT_PAIR {
    ULONGLONG Offset;
    ULONGLONG Length;
} EXTENT_PAIR, *PEXTENT_PAIR;

typedef struct _FILE_LEVEL_TRIM {
    //
    // A count of how many Offset:Length pairs are given
    //
    DWORD PairCount;
    //
    // All the pairs.
    //
    EXTENT_PAIR Pairs[1];
} FILE_LEVEL_TRIM, *PFILE_LEVEL_TRIM;
```



O arquivo de corte é passado por meio do buffer, se possível ou de forma assíncrona (sem buffer) para o comando de DSM do IOCTL do dispositivo. Isso é mapeado para o comando TRIM para dispositivos ATA e comando de desmapeamento para dispositivos SCSI. O código de corte do arquivo envia as regiões uma a uma conforme especificado pelas extensões acima.

O arquivo TRIM não espera por retornos do dispositivo, porque os comandos TRIM e removem são definidos como dicas para a mídia de armazenamento subjacente e os códigos de retorno não são esperados.

**Fluxo de trabalho de ponta a ponta:**

1.  Recortar arquivo de chamada
    1.  O arquivo de corte examina as entradas de erros
    2.  O corte de arquivo divide as extensões em regiões de LCN
    3.  O corte de arquivo é arredondado para cima e para baixo para regiões desalinhadas que são passadas para o corte
    4.  O corte de arquivo limpa as entradas no cache relacionadas às áreas de corte
    5.  O arquivo de corte passa \_ por IOCTL DSM (trim) por região
2.  Recorte de arquivo retorna ou erros
    1.  A verificação de erros é feita na validade de entrada
    2.  Se apenas algumas das extensões forem válidas, um erro será retornado para a chamada de API completa

**Casos de uso**

**VHD (disco rígido virtual) do consumidor montado em um SSD:**

Inicialmente, o VHD é montado em mídia não utilizada "limpa". Como o VHD é usado, o VHD consome partes da mídia de armazenamento para arquivos, etc. Quando ele exclui arquivos na mídia de armazenamento, esses arquivos não são removidos do SSD, pois o VHD completo é armazenado como um arquivo no SSD. O ambiente Hyper-V chama o corte de arquivo para todas as regiões que são excluídas quando Delete-File ocorre no ambiente VHD. As \_ aparas de arquivo são convertidas no SSD para que o desempenho do SSD possa ser otimizado.

**VHD de consumidor montado em uma SAN com provisionamento dinâmico:**

Inicialmente, o VHD é montado em uma laje mínima de um ambiente com provisionamento dinâmico. À medida que os arquivos são armazenados no VHD, a superfície de armazenamento do VHD cresce em múltiplos de Slabs. Quando os arquivos são removidos no VHD, o Hyper-V chama o arquivo de \_ corte para a San provisionada subjacente. Se os cortes forem maiores que a granularidade da laje, a SAN agora poderá remover uma laje e, portanto, reduzir a superfície do VHD nessa SAN.

Se o VHD for residente em um servidor baseado no Windows 8, o otimizador de armazenamento também enviará cortes para reduzir a superfície do Slab do VHD de dentro do VHD montado.

## <a name="tests"></a>Testes

Não há APIs comparáveis em versões anteriores do sistema operacional. Não deve haver impacto no desempenho da própria API propriamente dita, embora a mídia de armazenamento (se implementada corretamente) possa mostrar um melhor desempenho de gravação. A API deve ser usada com muito cuidado; somente as extensões que não forem mais necessárias devem ser passadas, pois essas extensões serão removidas permanentemente da mídia de armazenamento.

## <a name="resources"></a>Recursos

-   [Especificação de T13](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [Especificação de SCSI T10](https://www.t10.org/)

 

 





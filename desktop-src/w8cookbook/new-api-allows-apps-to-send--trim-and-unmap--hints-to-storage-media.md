---
title: A nova API permite que os aplicativos enviem dicas "TRIM e Unmap" para a mídia de armazenamento
description: A nova API permite que os aplicativos enviem \ 0034; TRIM e Unmap \ 0034; dicas para a mídia de armazenamento
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d79d47dceb5c8bf2e7575836c9a40ddf0347b7e5c616ab4b7196b547742c97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028824"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a>A nova API permite que os aplicativos enviem dicas "TRIM e Unmap" para a mídia de armazenamento

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

As dicas TRIM notificam a unidade de que determinados setores alocados anteriormente não são mais necessários para o aplicativo e podem ser limpos. Normalmente, isso é usado quando um aplicativo faz grandes alocações de espaço por meio de um arquivo e, em seguida, gerencia as alocações para o arquivo (por exemplo, arquivos de Disco Rígido Virtual).

**O que é TRIM?**

Os SSDs (unidades de estado sólido) normalmente são dispositivos apagados em bloco baseados em memória flash; isso significa que, quando os dados são gravados no SSD, eles não podem ser gravados em excesso no local e devem ser gravados em outro lugar até que o bloco possa ser coletado como lixo. Como o SSD não tem nenhum mecanismo interno para determinar que determinados blocos são removidos e outros são necessários. A única vez que o SSD pode marcar um setor 'sujo' é quando ele é gravado em excesso. Em outros casos, como quando um arquivo é excluído, o SSD retém esses setores porque a exclusão é executada apenas como uma alteração de MFT (tabela de arquivos mestre) e não como uma operação para todos os setores do arquivo. No Windows 7, introduzimos uma maneira padrão de se comunicar com SSDs sobre setores que não são mais necessários. Esse comando é definido na [especificação T13](https://www.t13.org/Standards/Default.aspx?DocumentType=3) como o comando TRIM; O NTFS envia o comando TRIM para algumas operações em linha normais, como "deletefile".

**Outros usos do TRIM no mundo do armazenamento**

Como SSDs, SANs (redes de área de armazenamento) e o novo recurso Windows 8 implementações de Espaços de Software consomem dicas de comando TRIM para gerenciar seus espaços em ambientes provisionados de forma fina. SaNs e Espaços de Software alocam regiões de armazenamento em tamanhos maiores que setores ou clusters (de 1 MB a 1 GB). Quando eles recebem dicas TRIM para seu tamanho de alocação (ou maior que o tamanho da alocação), o SAN/SSD pode desalocar uma região para liberar o espaço para outros arquivos. Normalmente, eles passam todas as dicas TRIM para a mídia subjacente (SSD ou HDD) para que possam consumir o espaço liberado conforme apropriado. Normalmente, eles não movem dados para regiões desalocadas nem acompanham as áreas TRIM para regiões desalocadas (quando a região está vazia).

SaNs provisionadas de forma fina usam as dicas TRIM passadas para ajudar a reduzir o espaço de armazenamento físico geral, reduzindo o custo. A [especificação SCSI T10](https://www.t10.org) define o comando 'Unmap' (semelhante ao comando TRIM); aqui, o comando é aplicável a todos os tipos de armazenamento, incluindo HDDs, SSDs e outros. O comando UnMap ajuda a remover blocos físicos da alocação da SAN.

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



O TRIM do arquivo é passado por meio do buffer, se possível ou de forma assíncrona (sem buffer) para o comando TRIM do DSM do IOCTL do Dispositivo. Isso é mapeado para o comando TRIM para dispositivos ATA e o comando UnMap para dispositivos SCSI. O código TRIM do arquivo envia as regiões um por um, conforme especificado pelas extensão acima.

O TRIM do arquivo não aguarda retornos do dispositivo, pois os comandos TRIM e Unmap são definidos como dicas para a mídia de armazenamento subjacente e os códigos de retorno não são esperados.

**Fluxo de trabalho de ponta a ponta:**

1.  Corte de arquivo de chamada
    1.  O TRIM do arquivo examina as entradas em busca de erros
    2.  O TRIM do arquivo divide as extensão em regiões LCN
    3.  O TRIM do arquivo arredopa para cima e para baixo para regiões alinhadas incompatibilidade que são passadas para TRIM
    4.  O TRIM do arquivo limpa as entradas no cache relacionadas às áreas TRIM
    5.  O TRIM de arquivo passa \_ IOCTL DSM (Corte) por região
2.  Retornos de TRIM de arquivo ou erros
    1.  A verificação de erro é feita na validade da entrada
    2.  Se apenas algumas das extensão são válidas, um erro é retornado para a chamada à API completa

**Casos de uso**

**VHD (disco rígido virtual) do consumidor montado em um SSD:**

O VHD é inicialmente montado em uma mídia 'limpa' nãoutilada. Como o VHD é usado, o VHD consome partes da mídia de armazenamento para arquivos etc. Quando ele exclui arquivos na mídia de armazenamento, esses arquivos não são removidos do SSD, pois o VHD completo é armazenado como um arquivo no SSD. O ambiente Hyper-V chama File TRIM para todas as regiões excluídas quando o arquivo de exclusão ocorre no ambiente VHD. Os \_ TRIMs de Arquivo são convertidos no SSD para que o desempenho do SSD possa ser otimizado.

**VHD do consumidor montado em uma SAN provisionada de forma fina:**

O VHD é inicialmente montado em uma laje mínima de um ambiente provisionado de forma fina. À medida que os arquivos são armazenados no VHD, o volume de armazenamento do VHD aumenta em múltiplos de lajes. Quando os arquivos são removidos no VHD, o Hyper-V chama File TRIM para a SAN provisionada de forma \_ fina subjacente. Se os TRIMs são maiores que a granularidade do SLAB, a SAN agora pode remover um SLAB e, portanto, reduzir o espaço do VHD nessa SAN.

Se o VHD for residente em um servidor baseado em Windows 8, o otimizador Armazenamento também enviará TRIMs para reduzir o espaço de trabalho do VHD de dentro do VHD montado.

## <a name="tests"></a>Testes

Não há APIs comparáveis em versões anteriores do sistema operacional. Não deve haver nenhum impacto no desempenho da própria API real, embora a mídia de armazenamento (se implementada corretamente) possa mostrar um melhor desempenho de gravação. A API deve ser usada com muito cuidado; somente as extensão que não são mais necessárias devem ser passadas para baixo, pois essas extensão serão removidas permanentemente da mídia de armazenamento.

## <a name="resources"></a>Recursos

-   [Especificação T13](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [Especificação do SCSI T10](https://www.t10.org/)

 

 





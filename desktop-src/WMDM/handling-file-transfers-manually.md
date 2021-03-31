---
title: Manipulando transferências de arquivos manualmente
description: Manipulando transferências de arquivos manualmente
ms.assetid: ff94191b-a0f2-4118-996c-d040f214fb9b
keywords:
- Windows Media Gerenciador de Dispositivos, transferências de arquivos manuais
- Gerenciador de Dispositivos, transferências de arquivos manuais
- Guia de programação, transferências de arquivos manuais
- aplicativos de área de trabalho, transferências de arquivos manuais
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, transferências de arquivos manuais
- transferências de arquivos manuais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2bf12404e8cd83b6f0c0e4f1c8ec8b0b7bda205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641509"
---
# <a name="handling-file-transfers-manually"></a>Manipulando transferências de arquivos manualmente

Seu aplicativo pode implementar a interface [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) para gerenciar parte do processo de leitura ou gravação. Em uma leitura do dispositivo, a implementação permite que o aplicativo receba blocos de dados brutos de um arquivo de dispositivo. Em uma gravação no dispositivo, ele permite que o aplicativo envie blocos de dados brutos para um arquivo no dispositivo.

Em operações de leitura e gravação, o método [**IWMDMOperation:: TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) passa os dados entre o computador e o dispositivo. Para saber a direção da transferência de dados, seu aplicativo deve definir um sinalizador quando o Windows Media Gerenciador de Dispositivos chama [**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) ou [**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite). Quando o método [**end**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) é chamado, o aplicativo deve redefinir esse sinalizador.

> [!Note]  
> Se o provedor de serviços e o dispositivo implementarem corretamente o [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2), ele primeiro chamará o método [IWMDMOperation3:: TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel) do aplicativo, se implementado. Esse método é uma maneira mais eficiente de transferir dados. **TransferObjectDataOnClearChannel** é manipulado da mesma maneira que **TransferObjectData**, exceto que os dados nunca são criptografados e não têm valores Mac para verificar.

 

As seções a seguir descrevem o processo de leitura e de gravação, quando seu aplicativo implementa **IWMDMOperation**.

**Lendo de um dispositivo**

Ao ler um arquivo de um dispositivo, o Windows Media Gerenciador de Dispositivos chama os seguintes métodos **IWMDMOperation** na ordem:

-   [**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) Chamado para notificar o aplicativo de que uma leitura do dispositivo está começando.
-   [**TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) Chamado uma ou mais vezes. O processamento de dados é descrito nas etapas a seguir:
    1.  O **TransferObjectData** recebe um buffer, *pData*, de tamanho *pdwSize* bytes, preenchidos com dados e um Mac para verificar os dados de entrada.
    2.  O aplicativo verifica os parâmetros de entrada com o MAC de entrada de dados.
    3.  O aplicativo descriptografa e lê a maior parte dos dados no *pData* como ele pode e modifica o valor retornado de *pdwSize* para indicar quantos bytes foram realmente lidos.
    4.  O aplicativo descriptografa os dados usando [**CSecureChannelClient::D ecryptparam**](/previous-versions/bb231586(v=vs.85))e os armazena ou usa-os, conforme necessário.
    5.  **TransferObjectData** retorna S \_ OK.
    6.  O Windows Media Gerenciador de Dispositivos continua a chamar **TransferObjectData** até que o aplicativo Leia todos os dados do arquivo ou o aplicativo retorna o WMDM \_ E o \_ usuário \_ cancelado para cancelar a operação (nesse caso, a leitura é cancelada e o Windows Media Gerenciador de dispositivos chama **end**).
-   [**Fim**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) Chamado para notificar o aplicativo de que uma leitura do dispositivo está terminando.

**Gravando em um dispositivo**

Ao gravar um arquivo no dispositivo, o Windows Media Gerenciador de Dispositivos chama os seguintes métodos **IWMDMOperation** na ordem:

-   [**Getobjectname**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectname) Chamado para permitir que o aplicativo especifique um nome para o novo armazenamento. Esse método só será chamado se o aplicativo não tiver especificado um nome no método **Insert** .
-   [**Getobjectattributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes) Chamado para permitir que o aplicativo especifique atributos para o novo armazenamento no dispositivo.
-   [**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite) Chamado para notificar que uma gravação no dispositivo está começando.
-   [**GetObjectTotalSize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjecttotalsize) Chamado para recuperar o tamanho total do objeto que está sendo gravado no dispositivo, para habilitar a otimização da transferência e também para dar ao Windows Media Gerenciador de Dispositivos uma oportunidade de cancelar a transferência se o arquivo for muito grande para o dispositivo.
-   [**TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) Chamado uma ou mais vezes. O processamento de dados é descrito nas etapas a seguir:
    1.  **TransferObjectData** recebe um ponteiro para um buffer de tamanho *pdwSize* bytes.
    2.  O aplicativo obtém um bloco de dados para enviar para o dispositivo, normalmente lendo dados de um arquivo e preenche o buffer recebido com até *pdwSize* bytes. Ele deve modificar *pdwSize* (se necessário) para refletir quantos bytes foram adicionados ao buffer.
    3.  O aplicativo cria um MAC de todos os parâmetros do método.
    4.  O aplicativo criptografa os dados no buffer, usando [**CSecureChannelClient:: EncryptParam**](/previous-versions/bb231587(v=vs.85)).
    5.  **TransferObjectData** retorna s \_ OK para indicar que há mais dados ou S \_ false para indicar que não há mais dados. Se o aplicativo retornar WMDM \_ e \_ usuário \_ cancelado, a operação de gravação será cancelada e o Windows Media Gerenciador de dispositivos chamará **end**.
    6.  O Windows Media Gerenciador de Dispositivos continua a chamar **TransferObjectData** enquanto o aplicativo retorna S \_ OK.
-   [**Fim**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) Chamado para notificar que uma gravação no dispositivo está terminando.

Para obter um exemplo de código, consulte [criptografia e descriptografia](encryption-and-decryption.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um aplicativo de Gerenciador de Dispositivos de mídia do Windows**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 
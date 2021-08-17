---
description: Este aplicativo de exemplo usa as APIs de áudio principais para alterar o volume do dispositivo, conforme especificado pelo usuário.
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c157149e6b15014b1228b2b5c97080fcdbdccd9acc2745ee5a986a7de7c997f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828267"
---
# <a name="endpointvolume"></a>EndpointVolume

Este aplicativo de exemplo usa as APIs de áudio principais para alterar o volume do dispositivo, conforme especificado pelo usuário.

Este tópico inclui as seções a seguir.

-   [Descrição](#description)
-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="description"></a>Descrição

Este exemplo demonstra os recursos a seguir.

-   [API MMDevice para](mmdevice-api.md) enumeração e seleção de dispositivo multimídia.
-   [EndpointVolume API](endpointvolume-api.md) para controlar os níveis de volume do ponto de extremidade do dispositivo.

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Localização    | Caminho/URL                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| SDK do Windows | \\Arquivos de \\ Programas SDKs da Microsoft Windows \\ v7.0 Exemplos de ponto de extremidade de \\ \\ áudio \\ \\ \\ multimídiaVolume... \\ |



 

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo x, use as seguintes etapas:

Para criar o exemplo EndpointVolumeChanger, use as seguintes etapas:

1.  Abra o shell do CMD para o SDK Windows e altere para o diretório de exemplo EndpointVolume.
2.  Execute o comando `start EndpointVolumeChanger.sln` no diretório EndpointVolume para abrir o projeto EndpointVolumeChanger na janela Visual Studio dados.
3.  Na janela, selecione a configuração **de solução Depurar** ou Liberar, selecione o menu **Build** na barra de menus e selecione a **opção Build.**  Se você não abrir Visual Studio shell do CMD para o SDK, Visual Studio terá acesso ao ambiente de build do SDK. Nesse caso, o exemplo não será criado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto WASAPIEndpointVolume.vcproj.

## <a name="running-the-sample"></a>Executando o exemplo

Se você criar o aplicativo de demonstração com êxito, um arquivo executável, EndpointVolumeChanger.exe, será gerado. Para executar, digite `EndpointVolumeChanger` uma janela de comando seguida por argumentos obrigatórios ou opcionais. O exemplo a seguir mostra como alternar a configuração de mute no dispositivo de console padrão.

`EndpointVolumeChanger.exe -console -m`

A tabela a seguir mostra os argumentos.

| Argumento        | Descrição                                                         |
|-----------------|---------------------------------------------------------------------|
| -?              | Mostra a ajuda.                                                         |
| -H              | Mostra a ajuda.                                                         |
| -+              | Incrementa o nível de volume no dispositivo de ponto de extremidade de áudio em uma etapa. . |
| -up             | Incrementa o nível de volume no dispositivo de ponto de extremidade de áudio em uma etapa.   |
| --              | Diminui o nível de volume no dispositivo de ponto de extremidade de áudio em uma etapa.   |
| -down           | Diminui o nível de volume no dispositivo de ponto de extremidade de áudio em uma etapa.   |
| -v              | Define o nível de volume mestre no dispositivo de ponto de extremidade de áudio.          |
| -console        | Use o dispositivo de console padrão.                                     |
| -communications | Use o dispositivo de comunicação padrão.                               |
| -multimídia     | Use o dispositivo multimídia padrão.                                  |
| -endpoint       | Use o identificador de ponto de extremidade especificado no valor da opção.          |



 

Se o aplicativo for executado sem argumentos, ele enumera os dispositivos disponíveis e solicita que o usuário selecione um dispositivo. Depois que o usuário especifica o dispositivo, o aplicativo exibe as configurações de volume atuais para o ponto de extremidade. O volume pode ser controlado usando as opções descritas na tabela anterior.

Para obter mais informações sobre como controlar os níveis de volume de dispositivos de ponto de extremidade de áudio, consulte [EndpointVolume API](endpointvolume-api.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK que usam as APIs de áudio principais](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 




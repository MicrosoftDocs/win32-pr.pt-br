---
description: Este aplicativo de exemplo usa as APIs de áudio principais para alterar o volume do dispositivo, conforme especificado pelo usuário.
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e89efe89035ec272c68c6a9289672a249616e23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457067"
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

-   [API MMDevice](mmdevice-api.md) para enumeração e seleção de dispositivo de multimídia.
-   [API EndpointVolume](endpointvolume-api.md) para controlar os níveis de volume do ponto de extremidade do dispositivo.

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Local    | Caminho/URL                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| SDK do Windows | \\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ EndpointVolume \\ ... |



 

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo x, use as seguintes etapas:

Para criar o exemplo de EndpointVolumeChanger, use as seguintes etapas:

1.  Abra o Shell CMD para o SDK do Windows e altere para o diretório de exemplo EndpointVolume.
2.  Execute o comando `start EndpointVolumeChanger.sln` no diretório EndpointVolume para abrir o projeto EndpointVolumeChanger na janela do Visual Studio.
3.  De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** . Se você não abrir o Visual Studio a partir do Shell CMD para o SDK, o Visual Studio não terá acesso ao ambiente de compilação do SDK. Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, WASAPIEndpointVolume. vcproj.

## <a name="running-the-sample"></a>Executando o exemplo

Se você criar o aplicativo de demonstração com êxito, um arquivo executável, EndpointVolumeChanger.exe, será gerado. Para executá-lo, digite `EndpointVolumeChanger` uma janela de comando seguida por argumentos obrigatórios ou opcionais. O exemplo a seguir mostra como alternar a configuração de mudo no dispositivo de console padrão.

`EndpointVolumeChanger.exe -console -m`

A tabela a seguir mostra os argumentos.

| Argumento        | Descrição                                                         |
|-----------------|---------------------------------------------------------------------|
| -?              | Mostra a ajuda.                                                         |
| -H              | Mostra a ajuda.                                                         |
| -+              | Incrementa o nível de volume no dispositivo de ponto de extremidade de áudio por uma etapa. . |
| -up             | Incrementa o nível de volume no dispositivo de ponto de extremidade de áudio por uma etapa.   |
| --              | Decrementa o nível de volume no dispositivo de ponto de extremidade de áudio por uma etapa.   |
| -para baixo           | Decrementa o nível de volume no dispositivo de ponto de extremidade de áudio por uma etapa.   |
| -v              | Define o nível de volume mestre no dispositivo de ponto de extremidade de áudio.          |
| -console        | Use o dispositivo de console padrão.                                     |
| -comunicações | Use o dispositivo de comunicação padrão.                               |
| -multimídia     | Use o dispositivo multimídia padrão.                                  |
| -ponto de extremidade       | Use o identificador de ponto de extremidade especificado no valor de opção.          |



 

Se o aplicativo for executado sem argumentos, ele enumerará os dispositivos disponíveis e solicitará que o usuário selecione um dispositivo. Depois que o usuário especifica o dispositivo, o aplicativo exibe as configurações de volume atuais para o ponto de extremidade. O volume pode ser controlado usando as opções descritas na tabela anterior.

Para obter mais informações sobre como controlar os níveis de volume de dispositivos de ponto de extremidade de áudio, consulte [API do EndpointVolume](endpointvolume-api.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK que usam as APIs de áudio principal](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 




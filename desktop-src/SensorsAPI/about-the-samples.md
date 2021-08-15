---
description: O Windows SDK inclui exemplos de código e ferramentas úteis para ajudá-lo a entender e usar a plataforma sensor e localização do Windows e as APIs relacionadas.
ms.assetid: e31174f6-1c2b-4d97-b6b6-e54825ff47f5
title: Sobre as amostras e ferramentas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5eecd388323ae8a548fcfefbc116224125b4b137f85231c56ea66235b3233fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890311"
---
# <a name="about-the-samples-and-tools"></a>Sobre as amostras e ferramentas

O Windows SDK inclui exemplos de código e ferramentas úteis para ajudá-lo a entender e usar a plataforma sensor e localização do Windows e as APIs relacionadas.

## <a name="samples"></a>Exemplos

O Windows SDK inclui os exemplos de API do sensor a seguir. Você pode encontrar os exemplos de API do Sensor na pasta chamada Amostras de sensores winui, em que você instalou o \\ \\ \\ SDK Windows aplicativo. Por exemplo, se você instalou o SDK do Windows na unidade C, encontrará os exemplos na seguinte pasta: C: Arquivos de Programas \\ \\ SDKs da Microsoft Windows \\ \\ v7.0 Amostras de sensores \\ \\ \\ winui.



| Nome da amostra       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AmbientLightAware | Este exemplo de MFC mostra como usar a API do Sensor lendo dados de sensores de luz ambiente no computador e alterando o tamanho do texto de acordo com as condições de iluminação. Você pode ver o código que mostra como gerenciar eventos e como solicitar permissões de usuário. Você também pode ver um exemplo de como gerenciar a interface do usuário com base em diferentes condições de iluminação. Para obter mais informações, consulte [Criando Light-Aware interfaces do usuário.](creating-light-aware-user-interfaces.md)<br/> Você deve ter Visual Studio 2008 instalado para criar este exemplo.<br/> |



 

Para obter mais informações, consulte o arquivo chamado ReadMe.txt que está incluído no exemplo.

Você também pode baixar o exemplo de AmbientLightAware da Galeria de Códigos. Para obter mais informações, consulte a página de download [do Ambient Light Aware.](/samples/browse/?redirectedfrom=MSDN-samples)

## <a name="tools"></a>Ferramentas

O Windows SDK inclui um sensor de luz virtual que você pode usar para simular um dispositivo de sensor de luz baseado em hardware. Você pode usar essa ferramenta para fornecer dados para o exemplo de AmbientLightAware para ver como o código no exemplo funciona.

A tabela a seguir descreve os arquivos que você deve usar para executar o sensor de luz virtual. Você pode encontrar esses arquivos na pasta chamada Bin, em que você instalou o SDK Windows. Por exemplo, se você instalou o SDK do Windows na unidade C em um computador de 32 bits, encontrará os arquivos de sensor de luz virtual na seguinte pasta: C: Arquivos de \\ Programas SDKs da Microsoft Windows \\ \\ \\ v7.0 \\ Bin. Em computadores de 64 bits, você deve usar a versão de 64 bits da ferramenta. No SDK Windows, as ferramentas de 64 bits estão localizadas na subpasta chamada x64.



| Nome do arquivo                    | Descrição                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| VirtualLightSensor.exe       | Este programa fornece um controle deslizante que permite alterar o nível dos dados claros que o sensor virtual relata. |
| VirtualLightSensorDriver.dll | O driver do sensor lógico que simula um sensor claro.                                                                       |
| VirtualLightSensorDriver.inf | O arquivo INF para o driver do sensor de luz virtual.                                                                              |



 

### <a name="installing-the-virtual-light-sensor"></a>Instalando o sensor de luz virtual

Antes de usar o aplicativo de sensor de luz virtual, você deve instalar o driver de sensor lógico. Siga estas etapas:

1.  Abra uma janela de comando como administrador.
2.  Altere para a Windows bin do SDK.
3.  Digite **pnputil -a VirtualLightSensorDriver.inf**.
4.  Quando solicitado, clique em **Instalar este software de driver de qualquer maneira.**
5.  Aguarde até que a janela de comando informe que o driver foi instalado com êxito.

### <a name="running-the-virtual-light-sensor"></a>Executando o sensor de luz virtual

Para executar o sensor de luz virtual, basta clicar duas vezes no arquivo .exe virtual. Certifique-se de habilitar o sensor, quando solicitado.

Ao executar o programa, você pode observar que há um atraso antes que o sensor fique disponível. A interface do usuário do sensor de luz virtual exibirá a mensagem "Aguardando" na barra de título, enquanto o gerenciador de sensor lógico cria um nó de dispositivo para o sensor lógico. Depois que a mensagem de espera desaparecer, você poderá usar o controle deslizante para definir o nível de saída do slide para o sensor de luz virtual.

A imagem a seguir mostra a interface do usuário do sensor de luz virtual em seu estado pronto.

![interface do usuário do sensor de luz virtual](images/virtuallightsensor.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre sensores lógicos](about-logical-sensors.md)
</dt> <dt>

[**LUZ \_ DA CATEGORIA DO \_ SENSOR**](sensor-category-light.md)
</dt> </dl>

 


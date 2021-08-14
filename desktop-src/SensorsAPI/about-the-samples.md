---
description: o SDK do Windows inclui exemplos de código e ferramentas úteis para ajudá-lo a entender e usar o Sensor de Windows e a plataforma de localização e as APIs relacionadas.
ms.assetid: e31174f6-1c2b-4d97-b6b6-e54825ff47f5
title: Sobre os exemplos e ferramentas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5eecd388323ae8a548fcfefbc116224125b4b137f85231c56ea66235b3233fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890311"
---
# <a name="about-the-samples-and-tools"></a>Sobre os exemplos e ferramentas

o SDK do Windows inclui exemplos de código e ferramentas úteis para ajudá-lo a entender e usar o Sensor de Windows e a plataforma de localização e as APIs relacionadas.

## <a name="samples"></a>Exemplos

o SDK do Windows inclui os exemplos de API do Sensor a seguir. você pode encontrar os exemplos de API do Sensor na pasta denominada \\ samples \\ winui \\ sensores, em que você instalou o SDK do Windows. por exemplo, se você instalou o SDK do Windows na unidade C, encontraria os exemplos na seguinte pasta: C: arquivos de \\ programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ winui \\ sensores.



| Nome da amostra       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AmbientLightAware | Este exemplo de MFC mostra como usar a API do sensor lendo dados de sensores de luz ambiente no computador e alterando o tamanho do texto de acordo com as condições de iluminação. Você pode ver o código que mostra como gerenciar eventos e como solicitar permissões de usuário. Você também pode ver um exemplo de como gerenciar a interface do usuário com base em condições de iluminação variáveis. Para obter mais informações, consulte [criando Light-Aware interfaces do usuário](creating-light-aware-user-interfaces.md).<br/> você deve ter o Visual Studio 2008 instalado para criar este exemplo.<br/> |



 

Para obter mais informações, consulte o arquivo chamado ReadMe.txt que está incluído no exemplo.

Você também pode baixar o exemplo de AmbientLightAware da Galeria de códigos. Para obter mais informações, consulte a página de download com [reconhecimento de luz ambiente](/samples/browse/?redirectedfrom=MSDN-samples) .

## <a name="tools"></a>Ferramentas

o SDK do Windows inclui um sensor de luz virtual que você pode usar para simular um dispositivo de sensor de luz baseado em hardware. Você pode usar essa ferramenta para fornecer dados para o exemplo de AmbientLightAware para ver como o código no exemplo funciona.

A tabela a seguir descreve os arquivos que você deve usar para executar o sensor de luz virtual. você pode encontrar esses arquivos na pasta denominada Bin, em que você instalou o SDK do Windows. por exemplo, se você instalou o SDK do Windows na unidade C em um computador de 32 bits, encontrará os arquivos do sensor de luz virtual na seguinte pasta: C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Bin. Em computadores de 64 bits, você deve usar a versão de 64 bits da ferramenta. no SDK do Windows, as ferramentas de 64 bits estão localizadas na subpasta chamada x64.



| Nome do arquivo                    | Descrição                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| VirtualLightSensor.exe       | Este programa fornece um controle deslizante que permite alterar o nível dos dados leves que o sensor virtual relata. |
| VirtualLightSensorDriver.dll | O driver de sensor lógico que simula um sensor de luz.                                                                       |
| VirtualLightSensorDriver. inf | O arquivo INF do driver do sensor de luz virtual.                                                                              |



 

### <a name="installing-the-virtual-light-sensor"></a>Instalando o sensor de luz virtual

Antes de usar o aplicativo sensor de luz virtual, você deve instalar o driver do sensor lógico. Siga estas etapas:

1.  Abra uma janela de comando como administrador.
2.  altere para a pasta Bin SDK do Windows.
3.  Digite **PnPUtil-a VirtualLightSensorDriver. inf**.
4.  Quando solicitado, clique em **instalar este driver de software mesmo assim**.
5.  Aguarde até que a janela de comando relate que o driver foi instalado com êxito.

### <a name="running-the-virtual-light-sensor"></a>Executando o sensor de luz virtual

Para executar o sensor de luz virtual, basta clicar duas vezes no arquivo .exe. Certifique-se de habilitar o sensor, quando solicitado.

Ao executar o programa, você pode observar que há um atraso antes que o sensor fique disponível. A interface do usuário do sensor de luz virtual exibirá a mensagem "aguardando" na barra de título enquanto o Gerenciador de sensor lógico criará um nó de dispositivo para o sensor lógico. Depois que a mensagem em espera desaparecer, você poderá usar o controle deslizante para definir o nível de saída Lux para o sensor de luz virtual.

A imagem a seguir mostra a interface do usuário do sensor de luz virtual em seu estado pronto.

![interface do usuário do sensor de luz virtual](images/virtuallightsensor.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre sensores lógicos](about-logical-sensors.md)
</dt> <dt>

[**\_luz da categoria do sensor \_**](sensor-category-light.md)
</dt> </dl>

 


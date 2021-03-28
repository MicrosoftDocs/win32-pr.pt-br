---
title: Renderizando um efeito (Direct3D 11)
description: Um efeito pode ser usado para armazenar informações ou para renderizar usando um grupo de estado.
ms.assetid: 7af239de-812d-4295-b599-b9deb371b01b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c99aef9f83cdf286e86ca843e57315d9ab88619
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366255"
---
# <a name="rendering-an-effect-direct3d-11"></a>Renderizando um efeito (Direct3D 11)

Um efeito pode ser usado para armazenar informações ou para renderizar usando um grupo de estado. Cada técnica especifica um conjunto de sombreadores de vértice, sombreadores envoltória, sombreadores de domínio, sombreadores de geometria, sombreadores de pixel, sombreadores de computação, estado do sombreador, estado de amostra e textura, estado de exibição de acesso não ordenado e outro Estado de pipeline. Assim, depois de organizar o estado em um efeito, você pode encapsular o efeito de renderização que resulta desse Estado criando e renderizando o efeito.

Há algumas etapas para preparar um efeito para a renderização. A primeira é compilar, que verifica o HLSL como código em relação à sintaxe da linguagem HLSL e às regras de estrutura de efeito. Você pode compilar um efeito do seu aplicativo usando chamadas à API ou pode compilar um efeito offline usando o utilitário de compilador de efeito [fxc.exe](/windows/desktop/direct3dtools/fxc). Depois que o efeito for compilado com êxito, crie-o chamando um conjunto diferente (mas muito semelhante) de APIs.

Depois que o efeito é criado, há duas etapas restantes para usá-lo. Primeiro, você deve inicializar os valores de estado de efeito (os valores das variáveis de efeito) usando vários métodos para definir o estado se eles não forem inicializados em HLSL. Para algumas variáveis, isso pode ser feito uma vez quando um efeito é criado; outras devem ser atualizadas sempre que seu aplicativo chamar o loop de renderização. Depois que as variáveis de efeito são definidas, você informa ao tempo de execução para renderizar o efeito aplicando uma técnica. Esses tópicos são discutidos mais detalhadamente abaixo.

Naturalmente, há considerações de desempenho para o uso de efeitos. Essas considerações são basicamente as mesmas se você não estiver usando um efeito. Coisas como minimizar a quantidade de alterações de estado e organizar as variáveis por frequência de atualização. Essas táticas são usadas para minimizar a quantidade de dados que precisam ser enviados da CPU para a GPU e, portanto, minimizar possíveis problemas de sincronização.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                        | Descrição                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Compilar um efeito](d3d11-graphics-programming-guide-effects-compile.md)<br/>         | Após a criação de um efeito, a próxima etapa é compilar o código para verificar se há problemas de sintaxe.<br/>                                                                                                                                                                                                          |
| [Criar um efeito](d3d11-graphics-programming-guide-effects-create.md)<br/>           | Um efeito é criado carregando o código de bytes de efeito compilado na estrutura de efeitos. Ao contrário dos efeitos 10, o efeito deve ser compilado antes da criação do efeito. Os efeitos carregados na memória podem ser criados chamando [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).<br/>                 |
| [Definir estado do efeito](d3d11-graphics-programming-guide-effects-set-state.md)<br/>        | Algumas constantes de efeito só precisam ser inicializadas. Depois de inicializado, o estado de efeito é definido como o dispositivo para todo o loop de processamento. Outras variáveis precisam ser atualizadas sempre que o loop de renderização é chamado. O código básico para definir variáveis de efeito é mostrado abaixo, para cada um dos tipos de variáveis.<br/> |
| [Aplicar uma técnica](d3d11-graphics-programming-guide-effects-apply-technique.md)<br/> | Com as constantes, texturas e o estado do sombreador declarados e inicializados, a única coisa que resta fazer é definir o estado do efeito no dispositivo.<br/>                                                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 


---
title: Renderizar um efeito (Direct3D 11)
description: Saiba mais sobre como renderizar um efeito para o Direct3D 11. Um efeito pode ser usado para armazenar informações ou renderizar usando um grupo de estado.
ms.assetid: 7af239de-812d-4295-b599-b9deb371b01b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3ba8ebbc1ac8989ac10568a00f26b26370c4bb8e7710098733dad74618e53af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117913596"
---
# <a name="rendering-an-effect-direct3d-11"></a>Renderizar um efeito (Direct3D 11)

Um efeito pode ser usado para armazenar informações ou renderizar usando um grupo de estado. Cada técnica especifica algum conjunto de sombreadores de vértice, sombreadores de chassi, sombreadores de domínio, sombreadores de geometria, sombreadores de pixel, sombreadores de computação, estado do sombreador, estado de amostra e textura, estado de exibição de acesso não organizado e outro estado de pipeline. Portanto, depois de organizar o estado em um efeito, você pode encapsular o efeito de renderização que resulta desse estado criando e renderizar o efeito.

Há algumas etapas para preparar um efeito para renderização. A primeira é a compilação, que verifica o código HLSL como em relação à sintaxe da linguagem HLSL e às regras da estrutura de efeito. Você pode compilar um efeito de seu aplicativo usando chamadas à API ou pode compilar um efeito offline usando o utilitário do compilador de [ efeitofxc.exe](/windows/desktop/direct3dtools/fxc). Depois que o efeito for compilado com êxito, crie-o chamando um conjunto diferente (mas muito semelhante) de APIs.

Depois que o efeito é criado, há duas etapas restantes para usá-lo. Primeiro, você deve inicializar os valores de estado de efeito (os valores das variáveis de efeito) usando vários métodos para definir o estado se eles não são inicializados em HLSL. Para algumas variáveis, isso pode ser feito uma vez quando um efeito é criado; outros devem ser atualizados sempre que seu aplicativo chamar o loop de renderização. Depois que as variáveis de efeito são definidas, você diz ao runtime para renderizar o efeito aplicando uma técnica. Todos esses tópicos são discutidos mais detalhadamente abaixo.

Naturalmente, há considerações de desempenho para usar efeitos. Essas considerações são, em grande parte, as mesmas se você não estiver usando um efeito. Coisas como minimizar a quantidade de alterações de estado e organizar as variáveis por frequência de atualização. Essas táticas são usadas para minimizar a quantidade de dados que precisam ser enviados da CPU para a GPU e, portanto, minimizar possíveis problemas de sincronização.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                        | Descrição                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Compilar um efeito](d3d11-graphics-programming-guide-effects-compile.md)<br/>         | Depois que um efeito tiver sido compilado, a próxima etapa será compilar o código para verificar se há problemas de sintaxe.<br/>                                                                                                                                                                                                          |
| [Criar um efeito](d3d11-graphics-programming-guide-effects-create.md)<br/>           | Um efeito é criado carregando o código de byte do efeito compilado na estrutura de efeitos. Ao contrário dos Efeitos 10, o efeito deve ser compilado antes de criar o efeito. Os efeitos carregados na memória podem ser criados chamando [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).<br/>                 |
| [Definir estado de efeito](d3d11-graphics-programming-guide-effects-set-state.md)<br/>        | Algumas constantes de efeito só precisam ser inicializadas. Depois de inicializado, o estado de efeito é definido como o dispositivo para todo o loop de renderização. Outras variáveis precisam ser atualizadas sempre que o loop de renderização é chamado. O código básico para definir variáveis de efeito é mostrado abaixo, para cada um dos tipos de variáveis.<br/> |
| [Aplicar uma técnica](d3d11-graphics-programming-guide-effects-apply-technique.md)<br/> | Com as constantes, as texturas e o estado do sombreador declarados e inicializados, a única coisa que resta fazer é definir o estado de efeito no dispositivo.<br/>                                                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 


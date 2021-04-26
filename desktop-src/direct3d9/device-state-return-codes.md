---
description: Uma lista de alguns dos códigos de retorno possíveis para métodos e funções.
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6cd860fcc8268bf2b63a9498b9960da359ca210
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999333"
---
# <a name="s_present"></a>S \_ presentes

Uma lista de alguns dos códigos de retorno possíveis para métodos e funções.



| \#definir                  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ OK                     | O dispositivo está em execução normalmente e pode ser usado para renderização.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_obstruído presente \_ S      | A área de apresentação é obstruído. Oclusão significa que a janela de apresentação está minimizada ou outro dispositivo entrou no modo de tela inteira no mesmo monitor que a janela de apresentação e a janela de apresentação está completamente no monitor. Oclusão não ocorrerá se a área do cliente for coberta por outra janela.<br/> Os aplicativos obstruído podem continuar a renderização e todas as chamadas terão sucesso, mas a janela de apresentação do obstruído não será atualizada. Preferivelmente, o aplicativo deve parar de renderizar para a janela de apresentação usando o dispositivo e continuar chamando [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) até s \_ OK ou o modo de execução \_ \_ \_ alterado.<br/> |
| modo de S \_ atual \_ \_ alterado | O modo de exibição da área de trabalho foi alterado. O aplicativo pode continuar renderizando, mas pode haver conversão/alongamento de cores. Escolha um formato de buffer de fundo semelhante ao modo de exibição atual e chame redefinir para recriar as cadeias de permuta. O dispositivo deixará esse estado depois que uma redefinição for chamada.                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Outros códigos de erro estão contidos em [D3DERR](d3derr.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 





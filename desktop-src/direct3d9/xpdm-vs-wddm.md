---
description: a API do Direct3D 9 opera no Windows XP display driver model (XPDM) ou no Windows Vista display driver model (WDDM), dependendo do sistema operacional instalado.
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM vs. WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0332198cd7c9425a3b5a107259dda1b1e974a04a2379244cdf939384260a89f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746046"
---
# <a name="xpdm-vs-wddm"></a>XPDM vs. WDDM

a API do Direct3D 9 opera no Windows XP display driver model (XPDM) ou no Windows Vista display driver model (WDDM), dependendo do sistema operacional instalado. Há algumas diferenças na maneira como a API do Direct3D se comporta nos dois modelos de driver.

-   [Proteger área de trabalho](#secure-desktop)
-   [Área de Trabalho Remota](#remote-desktop)
-   [Serviço do Windows](#windows-service)
-   [Tópicos relacionados](#related-topics)

## <a name="secure-desktop"></a>Proteger área de trabalho

a área de trabalho segura está ativa sempre que ocorrer qualquer uma das seguintes ações: o usuário bloqueia sua área de trabalho (Windows + L), a proteção de tela é ativada (quando nenhum usuário está conectado) ou por padrão quando o controle de conta de usuário apresenta um prompt. Quando a área de trabalho segura estiver ativa, o dispositivo HAL não estará acessível.

Diferenças entre XPDM e WDDM:

- A tentativa de criar um dispositivo de HAL de Direct3D9 falhará (com **D3DERR \_ não \_ disponível**) e qualquer dispositivo Direct3D 9 existente indicará um código de retorno de dispositivo perdido no presente.

- As APIs Direct3D9Ex e Direct3D 10 podem criar um dispositivo com êxito enquanto a área de trabalho segura está ativa e todas as chamadas para apresentar ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) ou dxgi) retornarão um código de status indicando que a área de trabalho não está disponível no momento.



 

## <a name="remote-desktop"></a>Área de Trabalho Remota

Quando uma área de trabalho remota está ativa, a exibição é tratada pela máquina de exibição com o computador de hospedagem enviando informações pela rede.

Diferenças entre XPDM e WDDM:

- No XPDM, todas as tentativas de criar um dispositivo Direct3D 9 em uma área de trabalho remota falharão.

- No WDDM, a área de trabalho remota dá suporte à criação de um dispositivo HAL em uma sessão de área de trabalho remota.



 

## <a name="windows-service"></a>Serviço do Windows

um serviço Windows é um processo executado em segundo plano, controlado pelo SCM (gerenciador de controle de serviço). Um serviço é executado independentemente do Active Desktop e, portanto, tem a capacidade limitada de interagir com os usuários.

Diferenças entre XPDM e WDDM:

- no WDDM, o isolamento da sessão 0 garante que um serviço não tenha acesso a qualquer área de trabalho do usuário como medida de segurança, portanto, um dispositivo de HAL do Direct3D 9 nunca estará disponível em um serviço Windows.



 

> [!Note]  
> não é possível usar o Direct3D 9 em um serviço Windows. Para obter mais informações, consulte [o artigo 978635 do suporte da Microsoft](https://support.microsoft.com/kb/978635).

 


A tabela a seguir resume as diferenças listadas aqui.



| Proteger área de trabalho | XPDM | WDDM (Direct3D9) | WDDM (Direct3D9Ex/Direct3D10) |
|-----------------|------|------------------|------------------------------|
| NULLREF         | Sim  | Sim              | Sim                          |
| HAL             | Não   | Não               | Sim                          |
| REF             | Sim  | Sim              | Sim                          |
| Área de Trabalho Remota  |      |                  |                              |
| NULLREF         | Não   | Sim              | Sim                          |
| HAL             | Não   | Sim              | Sim                          |
| REF             | Sim  | Sim              | Sim                          |
| Serviço do Windows |      |                  |                              |
| NULLREF         | Não   | Não               | Não                           |
| HAL             | Não   | Não               | Não                           |
| REF             | Não   | Não               | Não                           |
| WARP10          | N/D  | N/D              | Sim                          |



 

Para obter mais informações sobre XPDM, WDDM, Direct3D9Ex e Direct3D 10, consulte [APIs de gráficos no Windows](../direct3darticles/graphics-apis-in-windows-vista.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 

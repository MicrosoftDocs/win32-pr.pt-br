---
title: Interface do IMsRdpClientNonScriptable7
description: Fornece acesso às propriedades não programáveis da sessão remota de um cliente no controle ActiveX Área de Trabalho Remota. Deriva da interface IMsRdpClientNonScriptable6.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable7
- Serviços de Área de Trabalho Remota da interface IMsRdpClientNonScriptable7, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 8becf3bbf66ea18b2df87069ba38bab44c56db70
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "105791106"
---
# <a name="imsrdpclientnonscriptable7-interface"></a>Interface do IMsRdpClientNonScriptable7

Fornece acesso às propriedades não programáveis da sessão remota de um cliente no controle ActiveX Área de Trabalho Remota. Deriva da interface [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) . Os métodos desta interface só podem ser acessados por meio de vtable; Eles não estão disponíveis para uso em clientes programáveis.

Uma instância dessa interface é obtida chamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no objeto [**IMsTscAx**](imstscax-interface.md) , passando **\_ IMsRdpClientNonScriptable7 de IID**.

## <a name="members"></a>Membros

A interface **IMsRdpClientNonScriptable7** herda de [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md). **IMsRdpClientNonScriptable7** também tem estes tipos de membros:

- [Métodos](#methods)
- [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IMsRdpClientNonScriptable7** tem esses métodos.


| Método            | Descrição              |
|:------------------|:-------------------------|
| [**DisableDpiCursorScalingForProcess**](imsrdpclientnonscriptable7-disabledpicursorscalingforprocess.md)       |  Desabilita o dimensionamento local do cursor do mouse recebido do servidor, garantindo que a forma do cursor seja renderizada corretamente sem modificação.                   |

### <a name="properties"></a>Propriedades

A interface **IMsRdpClientNonScriptable7** tem essas propriedades.

| Propriedade         | Tipo de acesso           | Descrição            |
|:-----------------|:----------------------|:-----------------------|
| [**CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)      | Somente leitura |  Obtém a coleção de câmeras (e as configurações associadas) que estão disponíveis para redirecionamento.   |
| [**Área de Transferência**](imsrdpclientnonscriptable7-clipboard.md)                       | Somente leitura |    Obtém o controlador da área de transferência usado para sincronizar as áreas de transferência local e remota se a sincronização da área de transferência manual estiver habilitada.    |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|---------------------------------------|
| Cliente mínimo com suporte| Windows 10, versão 1803 (build 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| CLSID                    | CLSID \_ MsRdpClient12 é definido como 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8<br/> CLSID \_ MsRdpClient12NotSafeForScripting é definido como 3BB805C2-D9E2-4174-8A1E-C87D69563662<br/> CLSID \_ MsRdpClient11 é definido como 22A7E88C-5BF5-4DE6-B687-60F7331DF190<br/> CLSID \_ MsRdpClient11NotSafeForScripting é definido como 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8<br/>  |
| IID                      | IID \_ IMsRdpClientNonScriptable7 é definido como 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC            |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>

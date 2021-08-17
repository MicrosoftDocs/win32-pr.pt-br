---
title: Interface do IMsRdpClientNonScriptable7
description: Fornece acesso às propriedades nãoscriptáveis da sessão remota de um cliente no controle Área de Trabalho Remota ActiveX cliente. Deriva da interface IMsRdpClientNonScriptable6.
ms.tgt_platform: multiple
keywords:
- Interface IMsRdpClientNonScriptable7 Serviços de Área de Trabalho Remota
- Interface IMsRdpClientNonScriptable7 Serviços de Área de Trabalho Remota , descrita
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
ms.openlocfilehash: 01065ef73d1a23f0ac9416a39c4af74042c883e3b4d7f596cb95f6c01043f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117941103"
---
# <a name="imsrdpclientnonscriptable7-interface"></a>Interface do IMsRdpClientNonScriptable7

Fornece acesso às propriedades nãoscriptáveis da sessão remota de um cliente no controle Área de Trabalho Remota ActiveX cliente. Deriva da interface [**IMsRdpClientNonScriptable6.**](imsrdpclientnonscriptable6.md) Os métodos dessa interface só podem ser acessados por meio da vtable; eles não estão disponíveis para uso em clientes que podem ser scripts.

Uma instância dessa interface é obtida chamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no objeto [**IMsTscAx,**](imstscax-interface.md) passando **\_ IMsRdpClientNonScriptable7**.

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
| [**Área de Transferência**](imsrdpclientnonscriptable7-clipboard.md)                       | Somente leitura |    Obtém o controlador de área de transferência usado para sincronizar as áreas de transferência locais e remotas se a sincronização manual da área de transferência estiver habilitada.    |

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

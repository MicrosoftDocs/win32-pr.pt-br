---
title: Interface do IMsRdpClientNonScriptable6
description: Fornece acesso às propriedades não programáveis da sessão remota de um cliente no controle ActiveX Área de Trabalho Remota. Deriva da interface IMsRdpClientNonScriptable5.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable6
- Serviços de Área de Trabalho Remota da interface IMsRdpClientNonScriptable6, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 0d6793452ebf59f1974831aef0fa10f2469d8e92
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104370030"
---
# <a name="imsrdpclientnonscriptable6-interface"></a>Interface do IMsRdpClientNonScriptable6

Fornece acesso às propriedades não programáveis da sessão remota de um cliente no controle ActiveX Área de Trabalho Remota. Deriva da interface [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) . Os métodos desta interface só podem ser acessados por meio de vtable; Eles não estão disponíveis para uso em clientes programáveis.

Uma instância dessa interface é obtida chamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no objeto [**IMsTscAx**](imstscax-interface.md) , passando **\_ IMsRdpClientNonScriptable6 de IID**.

## <a name="members"></a>Membros

A interface **IMsRdpClientNonScriptable6** herda de [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md). **IMsRdpClientNonScriptable6** também tem estes tipos de membros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IMsRdpClientNonScriptable6** tem esses métodos.


| Método            | Descrição                   |
|:-----------------------------|:-----------------|
| [**SendLocation2D**](imsrdpclientnonscriptable6-sendlocation2d.md)     |  Envia um valor de latitude e longitude para o servidor para que a localização geográfica do cliente possa ser refletida na sessão remota.                   |
| [**SendLocation3D**](imsrdpclientnonscriptable6-sendlocation3d.md)     | Envia um valor de latitude, longitude e altitude para o servidor para que o local geográfico do cliente possa ser refletido na sessão remota.                 |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|---------------------------------------|
| Cliente mínimo com suporte| Windows 10, versão 1709 (build 16299)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| CLSID                    | CLSID \_ MsRdpClient12 é definido como 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8<br/> CLSID \_ MsRdpClient12NotSafeForScripting é definido como 3BB805C2-D9E2-4174-8A1E-C87D69563662<br/> CLSID \_ MsRdpClient11 é definido como 22A7E88C-5BF5-4DE6-B687-60F7331DF190<br/> CLSID \_ MsRdpClient11NotSafeForScripting é definido como 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8<br/>  |
| IID                      | IID \_ IMsRdpClientNonScriptable6 é definido como 05293249-B28B-4DB8-BE64-1B2F496B910E            |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

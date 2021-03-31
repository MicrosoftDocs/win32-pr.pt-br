---
description: Determina o comportamento de roaming de uma rede conectada automaticamente quando uma rede preferencial está no intervalo.
ms.assetid: 095dc797-1249-43aa-a8b7-5fa6eaee2a74
title: Elemento AutoSwitch (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- autoSwitch
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7ae05b18f58927e05c952edbbfc1b6a6190cec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827503"
---
# <a name="autoswitch-wlanprofile-element"></a>Elemento AutoSwitch (WLANProfile)

O elemento AutoSwitch (WLANProfile) determina o comportamento de roaming de uma rede conectada automaticamente quando uma rede preferencial está no intervalo. . Esse elemento é opcional.

Se AutoSwitch for "true" e [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) for definido como "auto", uma conexão com uma rede preferencial deverá ser tentada sempre que uma rede preferencial entrar em intervalo. Uma rede mais preferencial é aquela que é ordenada mais alta na lista de redes sem fio preferenciais. Essa tentativa de conexão ocorre quando conectado a outra rede.

Se [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) for definido como "auto", esse valor poderá ser "true" ou "false".

Se [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) for definido como "manual", esse valor deverá ser definido como "false". Este elemento não tem nenhum efeito em uma rede conectada manualmente.

Um valor de comutador AutoSwitch definido como "true" resulta em uma frequência mais alta de verificação periódica para novas redes. Isso pode resultar na maior poluição da freqüência de rádio dessas verificações periódicas e ao aumento do consumo de energia usado pelo adaptador de rede sem fio.

**Windows 7 e Windows Server 2008 R2 com o serviço de LAN sem fio instalado:** As alterações são implementadas no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado para otimizar o desempenho da rede sem fio. Essas alterações foram projetadas para reduzir a poluição da frequência de rádio, o consumo de energia e a interrupção no tráfego em tempo real em redes sem fio. A configuração padrão para **AutoSwitch** quando este elemento não está definido em um perfil de LAN sem fio foi alterado. A configuração padrão é alterada para "false" no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado. A configuração padrão era "true" no Windows Server 2008 e no Windows Vista. É recomendável que o valor do elemento de **comutador AutoSwitch** usado por um aplicativo em um perfil de LAN sem fio seja definido como "false" para reduzir a frequência de verificação periódica para novas redes, a menos que seja absolutamente necessário para um aplicativo definir esse valor como "true".

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.

``` syntax
<xs:element name="autoSwitch"
    type="boolean"
 />
```

O elemento **AutoSwitch** é definido pelo elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o elemento **AutoSwitch** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 





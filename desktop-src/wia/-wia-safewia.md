---
description: o objeto SafeWia é um &\# 0034; seguro para scripts&\# 0034; ponto de entrada para a funcionalidade de script da aquisição de imagem Windows (WIA).
ms.assetid: 6b10bb8e-8500-4f2c-ae18-5db78ef75f74
title: Objeto SafeWia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SafeWia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: ef324934abee38e2581b6e05c0fdac92145e4f43
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473842"
---
# <a name="safewia-object"></a>Objeto SafeWia

o objeto **SafeWia** é um ponto de entrada "seguro para scripts" para toda a funcionalidade de script da aquisição de imagem de Windows (WIA). Qualquer aplicativo que usa o modelo de script WIA deve criar um objeto **SafeWia** ou [**WIA**](-wia-wia.md) . Use esse objeto para enumerar e criar dispositivos e para receber notificações de eventos de hardware.

## <a name="members"></a>Membros

O objeto **SafeWia** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SafeWia** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Criar**](-wia-iwia-create.md) | O método [**Create**](-wia-iwia-create.md) do objeto [**WIA**](-wia-wia.md) faz uma conexão com o dispositivo WIA especificado e retorna um objeto [**Item**](-wia-item.md) que representa o dispositivo.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **SafeWia** tem essas propriedades.




| Propriedade | Tipo de acesso | Descrição | 
|----------|-------------|-------------|
| <a href="-wia-iwia-devices.md"><strong>Dispositivos</strong></a><br /> | Somente leitura<br /> | Coleção de objetos <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> que representa todos os dispositivos instalados no computador. Somente leitura. <br /><blockquote>[!Note]<br />Esta coleção é baseada em 0.</blockquote><br /> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |
| IID<br/>                      | \_SAFEWIA CLSID<br/>                                                                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WIA**](-wia-wia.md)
</dt> </dl>

 

 





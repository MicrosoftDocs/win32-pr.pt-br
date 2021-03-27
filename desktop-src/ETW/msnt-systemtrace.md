---
description: A classe pai da qual todas as classes de rastreamento de eventos do sistema são derivadas. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 27979d9c-eca7-426f-8f8e-99443e5a0188
title: Classe MSNT_SystemTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSNT_SystemTrace
- MSNT_SystemTrace.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2eb0044029761a93a353a08a955d39d76c267f9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967467"
---
# <a name="msnt_systemtrace-class"></a>\_Classe MSNT SystemTrace

A classe pai da qual todas as classes de rastreamento de eventos do sistema são derivadas.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{9e814aad-3204-11d2-9a82-006008a86939}")]
class MSNT_SystemTrace : EventTrace
{
  uint32 Flags;
};
```

## <a name="members"></a>Membros

A classe **MSNT \_ SystemTrace** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **MSNT \_ SystemTrace** tem essas propriedades.

<dl> <dt>

**Sinalizadores**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **DefineValues {" \_ \_ \_ processo de sinalizador de rastreamento de eventos", " \_ thread de sinalizador de rastreamento de eventos \_ \_ ", " \_ \_ carregamento de imagem do sinalizador de rastreamento de eventos", "contadores de processo de sinalizador de rastreamento de eventos" \_ \_ \_ \_ \_ \_ , " \_ sinalizador de rastreamento de eventos \_ \_ CSWITCH", " \_ \_ sinal de rastreamento de eventos \_ DPC", " \_ \_ \_ interrupção de sinalizador de rastreamento de eventos", " \_ sinalizador de rastreamento de evento \_ \_ SYSTEMCALL", "sinalizador de rastreamento de eventos \_ \_ \_ \_ e/s de disco", "sinalizador de rastreamento de eventos \_ \_ \_ \_ \_ e/s de arquivo de disco", "sinalizador de rastreamento de eventos, e/s de disco", "Dispatcher de sinalizador de rastreamento de eventos", "falha de página de sinalizador de rastreamento de eventos", \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ registro de sinalizador de rastreamento de evento "," \_ sinalizador de rastreamento de evento \_ \_ ALPC "," sinalizador de rastreamento de eventos \_ \_ \_ dividir \_ e/s "," \_ Driver de sinalizador de rastreamento de eventos " \_ \_ ," \_ \_ \_ perfil de sinalizador de rastreamento de eventos "," \_ \_ \_ \_ e/s de arquivo de sinalizador de rastreamento de eventos ", \_ \_ Flag \_ File \_ Io \_ init"}**, **ValueMap {"0x00000001", "0x00000002", "0x00000004", "0x00000008", "0x00000010", "0x00000020", "0x00000040", "0x00000080", "0x00000100" , "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000", "0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}**
</dt> </dl>

Habilite o sinalizador que indica os provedores de kernel habilitados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



 

 





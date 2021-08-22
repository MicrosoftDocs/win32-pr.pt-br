---
title: Estrutura de DSA_SEC_PAGE_INFO
description: Usado com a planilha do WM \_ ADSPROP \_ \_ criar e o WM \_ DSA \_ sheet \_ criar \_ mensagens de notificação para definir uma folha de propriedades secundária em um snap-in do Active Directory MMC.
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- Estrutura de DSA_SEC_PAGE_INFO Active Directory
- Ponteiro de estrutura de PDSA_SEC_PAGE_INFO Active Directory
topic_type:
- apiref
api_name:
- DSA_SEC_PAGE_INFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26fa3dcfb983de8e1052b319bac7c3a594e256b594847c32b553353e6caee17d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695644"
---
# <a name="dsa_sec_page_info-structure"></a>\_Estrutura de \_ informações da página DSA SEC \_

A estrutura de **\_ informações da \_ página \_ DSA SEC** é usada com a folha do [**WM \_ ADSPROP \_ \_ criar**](wm-adsprop-sheet-create.md) e o [**WM \_ DSA \_ sheet \_ criar \_**](wm-dsa-sheet-create-notify.md) mensagens de notificação para definir uma folha de propriedades secundária em um snap-in do Active Directory MMC.

> [!Note]  
> Essa estrutura não está definida em um arquivo de cabeçalho publicado. Para usar essa estrutura, defina-a no formato exato mostrado.

 

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DSA_SEC_PAGE_INFO {
  HWND          hwndParentSheet;
  DWORD         offsetTitle;
  DSOBJECTNAMES dsObjectNames;
} DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**hwndParentSheet**
</dt> <dd>

Contém o identificador de janela do pai da folha de propriedades secundária.

</dd> <dt>

**offsetTitle**
</dt> <dd>

Contém o deslocamento, em bytes, do início da estrutura de **\_ \_ \_ informações da página DSA s** para uma cadeia de caracteres Unicode terminada em nulo que contém o título da folha de propriedades secundária.

</dd> <dt>

**dsObjectNames**
</dt> <dd>

Contém uma estrutura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) que define a folha de propriedades secundária. Somente uma folha de propriedades secundária pode ser criada de cada vez, portanto a estrutura **DSOBJECTNAMES** pode conter apenas uma estrutura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**criação da planilha do WM \_ ADSPROP \_ \_**](wm-adsprop-sheet-create.md)
</dt> <dt>

[**\_notificação de \_ criação da folha DSA \_ do WM \_**](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 






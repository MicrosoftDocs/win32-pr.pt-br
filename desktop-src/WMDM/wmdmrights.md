---
title: Estrutura WMDMRIGHTS
description: A estrutura WMDMRIGHTS descreve os direitos de uso de conteúdo.
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- Estrutura WMDMRIGHTS Windows Media Gerenciador de Dispositivos
- Ponteiro de estrutura PWMDMRIGHTS Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDMRIGHTS
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8bc3bcd61efc64d32daa3179b77a9aaa518d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760905"
---
# <a name="wmdmrights-structure"></a>Estrutura WMDMRIGHTS

A estrutura **WMDMRIGHTS** descreve os direitos de uso de conteúdo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct __WMDMRIGHTS {
  UINT         cbSize;
  DWORD        dwContentType;
  DWORD        fuFlags;
  DWORD        fuRights;
  DWORD        dwAppSec;
  DWORD        dwPlaybackCount;
  WMDMDATETIME ExpirationDate;
} WMDMRIGHTS, *PWMDMRIGHTS;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamanho da estrutura, em bytes.

</dd> <dt>

**dwContentType**
</dt> <dd>

**DWORD** que contém o tipo de conteúdo.

</dd> <dt>

**fuFlags**
</dt> <dd>

Campo de bits especificando as opções de direitos em uso para o conteúdo.



| Valor                        | Descrição                                  |
|------------------------------|----------------------------------------------|
| \_PLAYBACKCOUNT de direitos do WMDM \_  | Número de vezes que o arquivo pode ser reproduzido. |
| \_EXPIRATIONDATE de direitos do WMDM \_ | Data de validade do arquivo.                 |
| \_FREESERIALIDS de direitos do WMDM \_  | Identificador de série livre do arquivo.          |
| \_Grupo GroupId de direitos do WMDM \_  | Identificador do arquivo.                      |
| \_NAMEDSERIALIDS de direitos do WMDM \_ | Identificador de série nomeado do arquivo.         |



 

</dd> <dt>

**fuRights**
</dt> <dd>

Campo de bits que contém os bits de direitos para o conteúdo.



| Valor                                     | Descrição                                   |
|-------------------------------------------|-----------------------------------------------|
| os \_ direitos \_ do WMDM são executados \_ no \_ PC                | O conteúdo pode ser reproduzido em um computador pessoal. |
| \_ \_ cópia de direitos \_ de WMDM para \_ \_ dispositivo não SDMI \_ | O conteúdo pode ser copiado para um dispositivo não SDMI.   |
| \_copiar direitos do WMDM \_ para o \_ \_ CD                | O conteúdo pode ser copiado para um CD.                |
| \_ \_ cópia de direitos \_ de WMDM para \_ \_ dispositivo SDMI      | O conteúdo pode ser copiado para um dispositivo SDMI.      |



 

</dd> <dt>

**dwAppSec**
</dt> <dd>

Matriz de bytes que especifica o nível mínimo de segurança do aplicativo.

</dd> <dt>

**dwPlaybackCount**
</dt> <dd>

**DWORD** que contém o número de horas restantes que o conteúdo pode ser renderizado.

</dd> <dt>

**ExpirationDate**
</dt> <dd>

Estrutura [**WMDMDATETIME**](wmdmdatetime.md) que contém a data e a hora de expiração do conteúdo. Se a licença não tiver uma data de expiração, o membro **Wano** será definido como 0xFFFF e todos os outros membros de **WMDMDATETIME** serão ignorados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMDSPStorage:: getrights**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[**IWMDMStorage:: getrights**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[**WMDMDATETIME**](wmdmdatetime.md)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 






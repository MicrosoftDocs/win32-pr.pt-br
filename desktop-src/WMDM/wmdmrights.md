---
title: Estrutura WMDMRIGHTS
description: A estrutura WMDMRIGHTS descreve os direitos de uso de conteúdo.
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- Estrutura WMDMRIGHTS windows Media Gerenciador de Dispositivos
- Ponteiro de estrutura PWMDMRIGHTS windows Media Gerenciador de Dispositivos
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
ms.openlocfilehash: 6b54713add3bef1c51d18fea3f66ac4b3e2e8ff1a066bcd83781f0f522d5a4be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583979"
---
# <a name="wmdmrights-structure"></a>Estrutura WMDMRIGHTS

A **estrutura WMDMRIGHTS** descreve os direitos de uso de conteúdo.

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

Campo de bits que especifica as opções de direitos em uso para o conteúdo.



| Valor                        | Descrição                                  |
|------------------------------|----------------------------------------------|
| WMDM \_ RIGHTS \_ PLAYBACKCOUNT  | Número de vezes que o arquivo pode ser interpretado. |
| EXPIRAÇÃO DE \_ DIREITOS DO WMDMDATE \_ | Data de validade do arquivo.                 |
| DIREITOS DO WMDM \_ \_ FREESERIALIDS  | Identificador serial gratuito do arquivo.          |
| Grupo \_ GROUPID DE DIREITOS DO WMDM \_  | Identificador do arquivo.                      |
| DIREITOS DO WMDM \_ \_ NAMEDSERIALIDS | Identificador serial nomeado do arquivo.         |



 

</dd> <dt>

**fuRights**
</dt> <dd>

Campo de bits que contém os bits de direitos para o conteúdo.



| Valor                                     | Descrição                                   |
|-------------------------------------------|-----------------------------------------------|
| WMDM \_ RIGHTS PLAY NO \_ \_ \_ PC                | O conteúdo pode ser interpretado em um computador pessoal. |
| CÓPIA DE DIREITOS DO WMDM \_ \_ PARA DISPOSITIVO NÃO \_ \_ \_ \_ SDMI | O conteúdo pode ser copiado para um dispositivo não SDMI.   |
| CÓPIA DE DIREITOS DO WMDM \_ \_ PARA \_ \_ CD                | O conteúdo pode ser copiado para um CD.                |
| CÓPIA DE DIREITOS DO WMDM \_ \_ PARA O DISPOSITIVO \_ \_ \_ SDMI      | O conteúdo pode ser copiado para um dispositivo SDMI.      |



 

</dd> <dt>

**dwAppSec**
</dt> <dd>

Matriz de byte que especifica o nível mínimo de segurança do aplicativo.

</dd> <dt>

**dwPlaybackCount**
</dt> <dd>

**DWORD** que contém o número de vezes restantes que o conteúdo pode ser renderizado.

</dd> <dt>

**ExpirationDate**
</dt> <dd>

[**Estrutura WMDMDATETIME**](wmdmdatetime.md) que contém a data de validade e a hora do conteúdo. Se a licença não tiver nenhuma data de validade, o **membro wYear** será definido como 0xFFFF e todos os outros membros de **WMDMDATETIME** serão ignorados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMDSPStorage::GetRights**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[**IWMDMStorage::GetRights**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[**WMDMDATETIME**](wmdmdatetime.md)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 






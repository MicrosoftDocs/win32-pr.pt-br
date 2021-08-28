---
title: Estrutura OPAQUECOMMAND
description: A estrutura OPAQUECOMMAND contém dados para comandos que são passados por meio do Gerenciador de Dispositivos de mídia do Windows para um dispositivo, mas não devem ser agidos pelo Windows Media Gerenciador de Dispositivos.
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- Estrutura OPAQUECOMMAND windows Media Gerenciador de Dispositivos
- estrutura windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- OPAQUECOMMAND
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d3f0b94146262c480e7e510497111bf82f0c020001717cb0000ee4a88df440
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904006"
---
# <a name="opaquecommand-structure"></a>Estrutura OPAQUECOMMAND

A **estrutura OPAQUECOMMAND** contém dados para comandos que são passados por meio do Gerenciador de Dispositivos de mídia do Windows para um dispositivo, mas não devem ser agidos pelo Windows Media Gerenciador de Dispositivos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct OPAQUECOMMAND {
  GUID  guidCommand;
  DWORD dwDataLen;
  BYTE  *pData;
  BYTE  abMAC[20];
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**guidCommand**
</dt> <dd>

**GUID** que representa o comando solicitado.

</dd> <dt>

**dwDataLen**
</dt> <dd>

Comprimento dos dados para os quais *pData* aponta, em bytes.

</dd> <dt>

**Pdata**
</dt> <dd>

Dados necessários para executar o comando e/ou dados retornados pelo comando.

</dd> <dt>

**abMAC \[ 20\]**
</dt> <dd>

Esse MAC (código de autenticação de mensagem) deve incluir o membro **guidCommand,** os dados aos quais *pdwDataLen* aponta e os dados para os quais *pData* aponta, se for o caso. Se *pData* for **NULL,** ele não deverá ser incluído no MAC. WMDM \_ MAC LENGTH é definido como \_ 20.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMDSPDevice::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-sendopaquecommand)
</dt> <dt>

[**IMDSPStorage::SendOpaqueCommands**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-sendopaquecommand)
</dt> <dt>

[**IWMDMDevice::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-sendopaquecommand)
</dt> <dt>

[**IWMDMStorage::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 






---
title: Estrutura OPAQUECOMMAND
description: A estrutura OPAQUECOMMAND contém dados para comandos que são passados pelo Windows Media Gerenciador de Dispositivos para um dispositivo, mas que não devem ser afetados pelo Windows Media Gerenciador de Dispositivos.
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- Estrutura OPAQUECOMMAND Windows Media Gerenciador de Dispositivos
- estruturar Gerenciador de Dispositivos de mídia do Windows
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
ms.openlocfilehash: 672147cb99336f95a1ced88a3cc6b8df977aec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813204"
---
# <a name="opaquecommand-structure"></a>Estrutura OPAQUECOMMAND

A estrutura **OPAQUECOMMAND** contém dados para comandos que são passados pelo windows media Gerenciador de dispositivos para um dispositivo, mas que não devem ser afetados pelo windows media Gerenciador de dispositivos.

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

Comprimento dos dados aos quais *pData* pontos, em bytes.

</dd> <dt>

**pData**
</dt> <dd>

Dados necessários para executar o comando e/ou dados retornados pelo comando.

</dd> <dt>

**abMAC \[ 20\]**
</dt> <dd>

Esse código de autenticação de mensagem (MAC) deve incluir o membro **guidCommand** , os dados aos quais *pdwDataLen* aponta e os dados aos quais *pData* aponta, se houver. Se *pData* for **nulo**, ele não deverá ser incluído no Mac. \_ \_ O comprimento de Mac do WMDM é definido como 20.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



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

 

 






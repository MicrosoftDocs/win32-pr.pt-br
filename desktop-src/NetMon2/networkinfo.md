---
description: A estrutura NETWORKINFO descreve uma NIC.
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: Estrutura NETWORKINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8917966d2e090417a95a9ca20158c6c5935bda3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663365"
---
# <a name="networkinfo-structure"></a>Estrutura NETWORKINFO

A estrutura NETWORKINFO descreve uma NIC.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _NETWORKINFO {
  BYTE    PermanentAddr[6];
  BYTE    CurrentAddr[6];
  ADDRESS OtherAddress;
  DWORD   LinkSpeed;
  DWORD   MacType;
  DWORD   MaxFrameSize;
  DWORD   Flags;
  DWORD   TimestampScaleFactor;
  BYTE    NodeName[32];
  BOOL    PModeSupported;
  BYTE    Comment[ADAPTER_COMMENT_LENGTH];
} NETWORKINFO, *LPNETWORKINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**PermanentAddr**
</dt> <dd>

Endereço MAC permanente.

</dd> <dt>

**CurrentAddr**
</dt> <dd>

Endereço MAC atual.

</dd> <dt>

**OtherAddress**
</dt> <dd>

Outro endereço que dá suporte a isso (por exemplo, IP, IPX).

</dd> <dt>

**LinkSpeed**
</dt> <dd>

Velocidade do link, em Mbps.

</dd> <dt>

**MacType**
</dt> <dd>

Tipo de mídia.

</dd> <dt>

**MaxFrameSize**
</dt> <dd>

Tamanho máximo de quadro permitido.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Esse parâmetro pode ser um dos seguintes sinalizadores informativos:



| Valor                                                                                                                                                                                                                                       | Significado                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <dt>**NETWORKINFO \_ flags \_ pmode \_ não \_ suportado**</dt> </dl>    | A placa de rede não dá suporte ao modo promíscuo, o que significa que ele capturará apenas o tráfego que é difundido por natureza ou apenas envolve o computador local.<br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <dt>**\_RAS de sinalizadores NETWORKINFO \_**</dt> </dl>                                                      | Essa é uma placa de rede virtual que é uma conexão RAS (servidor de acesso remoto) por meio de um modem ou outra placa de rede.<br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <dt>**\_ \_ cartão remoto de sinalizadores NETWORKINFO \_**</dt> </dl>                             | A placa de rede não está no computador local, mas está sendo capturada em um computador remoto no Bequest do computador local.<br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <dt>**\_ \_ nal remoto de sinalizadores NETWORKINFO \_**</dt> </dl>                                | Substituí Não use.<br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <dt>**NETWORKINFO \_ sinalizadores \_ remotos de \_ nal \_ conectados**</dt> </dl> | Substituí Não use.<br/>                                                                                                                                          |



 

</dd> <dt>

**TimestampScaleFactor**
</dt> <dd>

Por exemplo, um valor de 1 indica 1/1 ms, 10 indica 1/10 ms, 100 indica 1/100 ms e assim por diante.

</dd> <dt>

**NodeName**
</dt> <dd>

Nome da estação de trabalho remota.

</dd> <dt>

**PModeSupported**
</dt> <dd>

Indicador de suporte de modo P NIC.

</dd> <dt>

**Comentário**
</dt> <dd>

Campo de comentário do adaptador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 





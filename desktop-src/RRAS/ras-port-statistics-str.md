---
title: Estrutura de RAS_PORT_STATISTICS (Rassapi. h)
description: A estrutura de estatísticas de porta de RAS \_ \_ relata as estatísticas que um servidor RAS coleta para uma porta conectada.
ms.assetid: c42c7059-ff92-4f49-a86e-2f47a083aa8e
keywords:
- RAS da estrutura de RAS_PORT_STATISTICS
- RAS de ponteiro de estrutura de PRAS_PORT_STATISTICS
topic_type:
- apiref
api_name:
- RAS_PORT_STATISTICS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e60fb001da3f8401e47c366eecc86aced22b77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759603"
---
# <a name="ras_port_statistics-structure"></a>Estrutura de estatísticas de \_ porta de Ras \_

\[A estrutura de **\_ \_ Estatísticas de porta de Ras** não tem suporte no Windows Vista.\]

A estrutura de **\_ \_ Estatísticas de porta de Ras** relata as estatísticas que um servidor RAS coleta para uma porta conectada. O servidor RAS redefine os vários contadores de estatística cada vez que a porta é conectada. Chame a função [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) para forçar o servidor RAS a redefinir os contadores de estatística.

Para uma porta que faz parte de uma conexão Multilink, essa estrutura fornece dois conjuntos de estatísticas. O primeiro conjunto contém as estatísticas cumulativas para todas as portas na conexão. Essas estatísticas são as mesmas para todas as portas na conexão. O segundo conjunto contém as estatísticas apenas para essa porta. Se a porta não fizer parte de uma conexão Multilink, os dois conjuntos de estatísticas terão as mesmas informações. Para determinar se uma porta faz parte de uma conexão de vínculos múltiplos, verifique a porta de \_ bits com múltiplas conexões no membro **flags** da estrutura [**da \_ porta \_ 0 do RAS**](ras-port-0-str.md) da porta.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _RAS_PORT_STATISTICS {
  DWORD dwBytesXmited;
  DWORD dwBytesRcved;
  DWORD dwFramesXmited;
  DWORD dwFramesRcved;
  DWORD dwCrcErr;
  DWORD dwTimeoutErr;
  DWORD dwAlignmentErr;
  DWORD dwHardwareOverrunErr;
  DWORD dwFramingErr;
  DWORD dwBufferOverrunErr;
  DWORD dwBytesXmitedUncompressed;
  DWORD dwBytesRcvedUncompressed;
  DWORD dwBytesXmitedCompressed;
  DWORD dwBytesRcvedCompressed;
  DWORD dwPortBytesXmited;
  DWORD dwPortBytesRcved;
  DWORD dwPortFramesXmited;
  DWORD dwPortFramesRcved;
  DWORD dwPortCrcErr;
  DWORD dwPortTimeoutErr;
  DWORD dwPortAlignmentErr;
  DWORD dwPortHardwareOverrunErr;
  DWORD dwPortFramingErr;
  DWORD dwPortBufferOverrunErr;
  DWORD dwPortBytesXmitedUncompressed;
  DWORD dwPortBytesRcvedUncompressed;
  DWORD dwPortBytesXmitedCompressed;
  DWORD dwPortBytesRcvedCompressed;
} RAS_PORT_STATISTICS, *PRAS_PORT_STATISTICS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwBytesXmited**
</dt> <dd>

Especifica o número total de bytes transmitidos pela conexão.

</dd> <dt>

**dwBytesRcved**
</dt> <dd>

Especifica o número total de bytes recebidos pela conexão.

</dd> <dt>

**dwFramesXmited**
</dt> <dd>

Especifica o número total de quadros transmitidos pela conexão.

</dd> <dt>

**dwFramesRcved**
</dt> <dd>

Especifica o número total de quadros recebidos pela conexão.

</dd> <dt>

**dwCrcErr**
</dt> <dd>

Especifica o número total de erros de CRC na conexão. Os erros de CRC são causados pela falha de uma verificação de redundância cíclica. Um erro de CRC indica que um ou mais caracteres no pacote de dados recebidos foram encontrados ilegíveis na chegada.

</dd> <dt>

**dwTimeoutErr**
</dt> <dd>

Especifica o número total de erros de tempo limite na conexão. Os erros de tempo limite ocorrem quando um caractere esperado não é recebido no tempo. Quando isso ocorre, o software pressupõe que os dados foram perdidos e solicita que eles sejam reenviados.

</dd> <dt>

**dwAlignmentErr**
</dt> <dd>

Especifica o número total de erros de alinhamento na conexão. Os erros de alinhamento ocorrem quando um caractere recebido não é o esperado. Isso geralmente acontece quando um caractere é perdido ou quando ocorre um erro de tempo limite.

</dd> <dt>

**dwHardwareOverrunErr**
</dt> <dd>

Especifica o número total de erros de saturação de hardware na conexão. Esses erros indicam o número de vezes que o computador de envio transmitiu caracteres mais rápido do que o hardware do computador de recebimento pode processá-los. Se esse problema persistir, reduza a taxa de conexão de BPS no cliente.

</dd> <dt>

**dwFramingErr**
</dt> <dd>

Especifica o número total de erros de enquadramento na conexão. Um erro de enquadramento ocorre quando um caractere assíncrono é recebido com um bit de início ou de parada inválido.

</dd> <dt>

**dwBufferOverrunErr**
</dt> <dd>

Especifica o número total de erros de saturação de buffer na conexão. Um erro de saturação de buffer ocorre quando o computador de envio está transmitindo caracteres mais rápido do que o computador receptor pode acomodá-los. Se esse problema persistir, reduza a taxa de conexão de BPS no cliente.

</dd> <dt>

**dwBytesXmitedUncompressed**
</dt> <dd>

Especifica o número total de bytes transmitidos não compactados pela conexão.

</dd> <dt>

**dwBytesRcvedUncompressed**
</dt> <dd>

Especifica o número total de bytes recebidos descompactados pela conexão.

</dd> <dt>

**dwBytesXmitedCompressed**
</dt> <dd>

Especifica o número total de bytes transmitidos compactados pela conexão.

</dd> <dt>

**dwBytesRcvedCompressed**
</dt> <dd>

Especifica o número total de bytes recebidos compactados pela conexão.

</dd> <dt>

**dwPortBytesXmited**
</dt> <dd>

Especifica o número total de bytes transmitidos pela porta.

</dd> <dt>

**dwPortBytesRcved**
</dt> <dd>

Especifica o número total de bytes recebidos pela porta.

</dd> <dt>

**dwPortFramesXmited**
</dt> <dd>

Especifica o número total de quadros transmitidos pela porta.

</dd> <dt>

**dwPortFramesRcved**
</dt> <dd>

Especifica o número total de quadros recebidos pela porta.

</dd> <dt>

**dwPortCrcErr**
</dt> <dd>

Especifica o número total de erros de CRC na porta. Os erros de CRC são causados pela falha de uma verificação de redundância cíclica. Um erro de CRC indica que um ou mais caracteres no pacote de dados recebidos foram encontrados ilegíveis na chegada.

</dd> <dt>

**dwPortTimeoutErr**
</dt> <dd>

Especifica o número total de erros de tempo limite na porta. Os erros de tempo limite ocorrem quando um caractere esperado não é recebido no tempo. Quando isso ocorre, o software pressupõe que os dados foram perdidos e solicita que eles sejam reenviados.

</dd> <dt>

**dwPortAlignmentErr**
</dt> <dd>

Especifica o número total de erros de alinhamento na porta. Os erros de alinhamento ocorrem quando um caractere recebido não é o esperado. Isso geralmente acontece quando um caractere é perdido ou quando ocorre um erro de tempo limite.

</dd> <dt>

**dwPortHardwareOverrunErr**
</dt> <dd>

Especifica o número total de erros de saturação de hardware na porta. Esses erros indicam o número de vezes que o computador de envio transmitiu caracteres mais rápido do que o hardware do computador de recebimento pode processá-los. Se esse problema persistir, reduza a taxa de conexão de BPS no cliente.

</dd> <dt>

**dwPortFramingErr**
</dt> <dd>

Especifica o número total de erros de enquadramento na porta. Um erro de enquadramento ocorre quando um caractere assíncrono é recebido com um bit de início ou de parada inválido.

</dd> <dt>

**dwPortBufferOverrunErr**
</dt> <dd>

Especifica o número total de erros de saturação de buffer na porta. Um erro de saturação de buffer ocorre quando o computador de envio está transmitindo caracteres mais rápido do que o computador receptor pode acomodá-los. Se esse problema persistir, reduza a taxa de conexão de BPS no cliente.

</dd> <dt>

**dwPortBytesXmitedUncompressed**
</dt> <dd>

Especifica o número total de bytes transmitidos não compactados pela porta. Se a porta fizer parte de uma conexão Multilink, esse membro não será válido. Em vez disso, use as estatísticas de compactação para a conexão.

</dd> <dt>

**dwPortBytesRcvedUncompressed**
</dt> <dd>

Especifica o número total de bytes recebidos descompactados pela porta. Se a porta fizer parte de uma conexão Multilink, esse membro não será válido. Em vez disso, use as estatísticas de compactação para a conexão.

</dd> <dt>

**dwPortBytesXmitedCompressed**
</dt> <dd>

Especifica o número total de bytes transmitidos compactados pela porta. Se a porta fizer parte de uma conexão Multilink, esse membro não será válido. Em vez disso, use as estatísticas de compactação para a conexão.

</dd> <dt>

**dwPortBytesRcvedCompressed**
</dt> <dd>

Especifica o número total de bytes recebidos compactados pela porta. Se a porta fizer parte de uma conexão Multilink, esse membro não será válido. Em vez disso, use as estatísticas de compactação para a conexão.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do serviço de acesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Estruturas de administração do servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**\_Porta RAS \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortClearStatistics**](rasadminportclearstatistics.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 






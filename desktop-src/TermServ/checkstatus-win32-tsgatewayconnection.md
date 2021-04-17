---
title: Método CheckStatus da classe Win32_TSGatewayConnection
description: Verifica o status de uma conexão de servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota) com outro computador e determina se o computador de destino está configurado para balanceamento de carga.
ms.assetid: e8ee3d40-76eb-401f-b255-bccd7ba8c058
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CheckStatus
- Método CheckStatus Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnection
- Classe Win32_TSGatewayConnection Serviços de Área de Trabalho Remota, método CheckStatus
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.CheckStatus
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babb083af5c0581abe27d442a466c3d6114b957a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761334"
---
# <a name="checkstatus-method-of-the-win32_tsgatewayconnection-class"></a>Método CheckStatus da classe Win32 \_ TSGatewayConnection

Verifica o status de uma conexão de servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota) com outro computador e determina se o computador de destino está configurado para balanceamento de carga.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CheckStatus(
  [in] string ServerName,
  [in] string EndPointName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do Server* \[ no\]
</dt> <dd>

O nome do servidor de gateway RD de origem do qual a conexão é verificada.

</dd> <dt>

*Ponto de extremidade* \[ no\]
</dt> <dd>

O nome do servidor de destino (o ponto de extremidade) ao qual o acesso é verificado no servidor de origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna os seguintes valores de retorno possíveis.

<dl> <dt>


</dt> <dd>

0

O status da conexão é OK. O ponto de extremidade está acessível e está configurado para balanceamento de carga.

</dd> <dt>


</dt> <dd>

1

O status da conexão é desconhecido. Provavelmente, ocorreu uma exceção.

</dd> <dt>


</dt> <dd>

0x80075c34

O ponto de extremidade não pode ser acessado ou não está configurado para balanceamento de carga.

</dd> <dt>


</dt> <dd>

0x80075c32

Ocorreu um erro de status. O ponto de extremidade está acessível, mas o serviço de balanceamento de carga RPC/HTTP (RPCHTTPLBS) não foi iniciado no computador de destino.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TS. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> </dl>

 


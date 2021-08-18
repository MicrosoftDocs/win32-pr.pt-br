---
description: Recupera uma máscara de bits que identifica os conjuntos de produtos disponíveis no sistema. Se essa função for chamada em um aplicativo que é executado no contexto de um silo de servidores, a máscara do pacote para o silo do servidor será recuperada.
ms.assetid: 1D6434FD-D7BD-45F9-B7C3-238890AF9928
title: Função RtlGetSuiteMask (Ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetSuiteMask
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: c6a71a2cb697021edcf8cea3da8759bbe40aa8ed9be2a93f8adcbeba4197ef88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763465"
---
# <a name="rtlgetsuitemask-function"></a>Função RtlGetSuiteMask

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Recupera uma máscara de bits que identifica os conjuntos de produtos disponíveis no sistema. Se essa função for chamada em um aplicativo que é executado no contexto de um silo de servidores, a máscara do pacote para o silo do servidor será recuperada.

## <a name="syntax"></a>Sintaxe


```C++
ULONG NTAPI RtlGetSuiteMask(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Uma máscara de bits que identifica os conjuntos de produtos disponíveis no sistema. A máscara de bits pode incluir os valores a seguir.



| Valor retornado                                                                          | Descrição                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl> | O Microsoft Small Business Server já foi instalado no sistema, mas pode ter sido atualizado para outra versão do Windows. Consulte a seção comentários para obter mais informações sobre este sinalizador de bit.<br/>                                           |
| <dl> <dt>0x00000002</dt> </dl> | Windows 10 Enterprise, Windows 8.1 Enterprise, Windows server 2008 Enterprise, Windows server 2003, Edição Enterprise ou Windows 2000 Advanced server está instalado. Consulte a seção comentários para obter mais informações sobre este sinalizador de bit.<br/> |
| <dl> <dt>0x00000004</dt> </dl> | Os componentes do Microsoft BackOffice são instalados.<br/>                                                                                                                                                                                               |
| <dl> <dt>0x00000008</dt> </dl> | O Communications Server 2003, o Communications Server 2005, o Communications Server 2007 ou o Communications Server 2007 R2 está instalado.<br/>                                                                                                           |
| <dl> <dt>0x00000010</dt> </dl> | Os serviços de terminal estão instalados. Esse valor é sempre definido.<br/> Se **TerminalServer** for definido, mas **SingleUserTS** não estiver definido, o sistema estará sendo executado no modo de servidor de aplicativos.<br/>                                                         |
| <dl> <dt>0x00000020</dt> </dl> | O Microsoft Small Business Server é instalado com a licença de cliente restritiva em vigor. Consulte a seção comentários para obter mais informações sobre este sinalizador de bit.<br/>                                                                            |
| <dl> <dt>0x00000040</dt> </dl> | Windows O XP Embedded está instalado.<br/>                                                                                                                                                                                                            |
| <dl> <dt>0x00000080</dt> </dl> | Windows o server 2008 datacenter, o Windows server 2003, o datacenter Edition ou o Windows 2000 datacenter server está instalado.<br/>                                                                                                                     |
| <dl> <dt>0x00000100</dt> </dl> | Há suporte para Área de Trabalho Remota, mas há suporte para apenas uma sessão interativa. Esse valor é definido, a menos que o sistema esteja sendo executado no modo de servidor de aplicativos.<br/>                                                                                       |
| <dl> <dt>0x00000200</dt> </dl> | Windows o vista home Premium, Windows vista home Basic ou Windows XP home Edition está instalado.<br/>                                                                                                                                               |
| <dl> <dt>0x00000400</dt> </dl> | Windows O Server 2003, Web Edition está instalado.<br/>                                                                                                                                                                                               |
| <dl> <dt>0x00002000</dt> </dl> | Windows Armazenamento server 2003 R2 ou Windows Armazenamento server 2003 está instalado.<br/>                                                                                                                                                                  |
| <dl> <dt>0x00004000</dt> </dl> | Windows Server 2003, o Compute Cluster Edition está instalado.<br/>                                                                                                                                                                                   |
| <dl> <dt>0x00008000</dt> </dl> | Windows O servidor primário está instalado.<br/>                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Comentários

Você não deve confiar apenas no sinalizador 0x00000001 para determinar se o Small Business Server foi instalado no sistema, pois esse sinalizador e o sinalizador 0x00000020 são definidos quando esse pacote de produto é instalado. se você atualizar essa instalação para Windows Server, Edição Standard, o sinalizador 0x00000020 será limpo, no entanto, o sinalizador 0x00000001 permanecerá definido. Nesse caso, isso indica que o Small Business Server já foi instalado neste sistema. se essa instalação for mais atualizada para o Windows Server, Edição Enterprise, o sinalizador 0x00000001 permanecerá definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2016 \[ somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Ntddk. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 





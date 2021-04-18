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
ms.openlocfilehash: ed8d8906273d18125131251636bc6199d166547b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753077"
---
# <a name="rtlgetsuitemask-function"></a>Função RtlGetSuiteMask

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

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
| <dl> <dt>0x00000002</dt> </dl> | O Windows 10 Enterprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition ou Windows 2000 Advanced Server está instalado. Consulte a seção comentários para obter mais informações sobre este sinalizador de bit.<br/> |
| <dl> <dt>0x00000004</dt> </dl> | Os componentes do Microsoft BackOffice são instalados.<br/>                                                                                                                                                                                               |
| <dl> <dt>0x00000008</dt> </dl> | O Communications Server 2003, o Communications Server 2005, o Communications Server 2007 ou o Communications Server 2007 R2 está instalado.<br/>                                                                                                           |
| <dl> <dt>0x00000010</dt> </dl> | Os serviços de terminal estão instalados. Esse valor é sempre definido.<br/> Se **TerminalServer** for definido, mas **SingleUserTS** não estiver definido, o sistema estará sendo executado no modo de servidor de aplicativos.<br/>                                                         |
| <dl> <dt>0x00000020</dt> </dl> | O Microsoft Small Business Server é instalado com a licença de cliente restritiva em vigor. Consulte a seção comentários para obter mais informações sobre este sinalizador de bit.<br/>                                                                            |
| <dl> <dt>0x00000040</dt> </dl> | O Windows XP Embedded está instalado.<br/>                                                                                                                                                                                                            |
| <dl> <dt>0x00000080</dt> </dl> | O Windows Server 2008 Datacenter, o Windows Server 2003, o Datacenter Edition ou o Windows 2000 Datacenter Server está instalado.<br/>                                                                                                                     |
| <dl> <dt>0x00000100</dt> </dl> | Há suporte para Área de Trabalho Remota, mas há suporte para apenas uma sessão interativa. Esse valor é definido, a menos que o sistema esteja sendo executado no modo de servidor de aplicativos.<br/>                                                                                       |
| <dl> <dt>0x00000200</dt> </dl> | O Windows Vista Home Premium, o Windows Vista Home Basic ou o Windows XP Home Edition está instalado.<br/>                                                                                                                                               |
| <dl> <dt>0x00000400</dt> </dl> | O Windows Server 2003, Web Edition está instalado.<br/>                                                                                                                                                                                               |
| <dl> <dt>0x00002000</dt> </dl> | O Windows Storage Server 2003 R2 ou o Windows Storage Server 2003 está instalado.<br/>                                                                                                                                                                  |
| <dl> <dt>0x00004000</dt> </dl> | O Windows Server 2003, Compute Cluster Edition, está instalado.<br/>                                                                                                                                                                                   |
| <dl> <dt>0x00008000</dt> </dl> | O Windows Home Server está instalado.<br/>                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Comentários

Você não deve confiar apenas no sinalizador 0x00000001 para determinar se o Small Business Server foi instalado no sistema, pois esse sinalizador e o sinalizador 0x00000020 são definidos quando esse pacote de produto é instalado. Se você atualizar essa instalação para o Windows Server, Standard Edition, o sinalizador 0x00000020 será limpo, no entanto, o sinalizador 0x00000001 permanecerá definido. Nesse caso, isso indica que o Small Business Server já foi instalado neste sistema. Se essa instalação for atualizada ainda mais para o Windows Server, Enterprise Edition, o sinalizador 0x00000001 permanecerá definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Ntddk. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 





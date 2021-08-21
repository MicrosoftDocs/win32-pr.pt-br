---
description: Cria uma nova instância de ClusterShare do Win32 \_ .
ms.assetid: a6fde28d-f19e-4a31-8f0d-35927c75a030
ms.tgt_platform: multiple
title: Método Create da classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: edaafa00f792cf01b4166d525171cf15b7f781c8c0c943c17377b3bd9b3401dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020584"
---
# <a name="create-method-of-the-win32_clustershare-class"></a>Método Create da classe Win32 \_ ClusterShare

Cria uma nova instância de [**\_ ClusterShare do Win32**](win32-clustershare.md) .

## <a name="syntax"></a>Sintaxe


```mof
static uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Caminho* \[ do no\]
</dt> <dd>

caminho Local do compartilhamento de Windows.

Exemplo, "C: \\ arquivos de programas".

</dd> <dt>

*Nome* \[ do no\]
</dt> <dd>

O alias para um caminho configurado como um compartilhamento em um sistema de computador que executa o Windows.

Exemplo, "público".

</dd> <dt>

*Tipo* \[ de no\]
</dt> <dd>

Tipo de recurso que está sendo compartilhado. Os tipos incluem: unidades de disco, filas de impressão, IPC (comunicações entre processos) e dispositivos gerais.

<dt>

0 (0x0)
</dt> <dd>

Unidade de disco

</dd> <dt>

1 (0x1)
</dt> <dd>

Fila de impressão

</dd> <dt>

2 (0x2)
</dt> <dd>

Dispositivo

</dd> <dt>

3 (0x3)
</dt> <dd>

IPC

</dd> <dt>

2147483648 (0x80000000)
</dt> <dd>

Administrador da unidade de disco

</dd> <dt>

2147483649 (0x80000001)
</dt> <dd>

Administrador da fila de impressão

</dd> <dt>

2147483650 (0x80000002)
</dt> <dd>

Administrador do dispositivo

</dd> <dt>

2147483651 (0x80000003)
</dt> <dd>

Administrador de IPC

</dd> </dl> </dd> <dt>

*MaximumAllowed* \[ em, opcional\]
</dt> <dd>

Limite do número máximo de usuários com permissão para usar este recurso simultaneamente.

</dd> <dt>

*Descrição* \[ do em, opcional\]
</dt> <dd>

Descrição do objeto.

</dd> <dt>

*Senha* \[ do em, opcional\]
</dt> <dd>

TBD

</dd> <dt>

*Acesso* \[ ao em, opcional\]
</dt> <dd>

Instância incorporada opcional de uma classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) que contém o descritor de segurança para o novo compartilhamento.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ClusterShare Win32**](win32-clustershare.md)
</dt> </dl>

 


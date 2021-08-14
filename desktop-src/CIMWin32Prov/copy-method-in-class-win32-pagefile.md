---
description: Copia o arquivo de paginação lógica ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.
ms.assetid: e1ff3e91-dc30-4849-b80a-8838b527ad63
ms.tgt_platform: multiple
title: Método Copy da classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f078e040a356cd575dfc222c9c13548737d8846ad9c211ff1dedc334faee1cb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118419670"
---
# <a name="copy-method-of-the-win32_pagefile-class"></a>Método Copy da classe de \_ arquivo de paginação Win32

O método **Copy** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) copia o diretório ou o arquivo de paginação lógica especificado no caminho do objeto para o local especificado pelo parâmetro de entrada. Não haverá suporte para uma cópia se a substituição de um arquivo lógico existente for necessária.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do arquivo* \[ no\]
</dt> <dd>

Nome totalmente qualificado da cópia do arquivo (ou diretório).

Exemplo: c: \\ temp \\ newdirectory

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) se o arquivo foi copiado com êxito e qualquer outro número para indicar um erro.

<dl> <dt>

**0**
</dt> <dd>

A solicitação foi bem-sucedida.

</dd> <dt>

**2**
</dt> <dd>

Acesso negado.

</dd> <dt>

**8**
</dt> <dd>

Ocorreu uma falha não especificada.

</dd> <dt>

**9**
</dt> <dd>

O nome especificado não era válido.

</dd> <dt>

**10**
</dt> <dd>

O objeto especificado já existe.

</dd> <dt>

**11**
</dt> <dd>

O sistema de arquivos não é NTFS.

</dd> <dt>

**12**
</dt> <dd>

A plataforma não é Windows.

</dd> <dt>

**13**
</dt> <dd>

A unidade não é a mesma.

</dd> <dt>

**14**
</dt> <dd>

O diretório não está vazio.

</dd> <dt>

**15**
</dt> <dd>

Houve uma violação de compartilhamento.

</dd> <dt>

**16**
</dt> <dd>

O arquivo de inicialização especificado não era válido.

</dd> <dt>

**17**
</dt> <dd>

Um privilégio necessário para a operação não é mantido.

</dd> <dt>

**Abril**
</dt> <dd>

Um parâmetro especificado não é válido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Arquivo de paginação Win32**](win32-pagefile.md)
</dt> </dl>

 


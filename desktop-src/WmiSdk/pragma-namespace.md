---
description: Solicita que o compilador carregue o arquivo MOF no namespace especificado como NamespacePath. Se a opção de namespace do compilador MOF-n e o \# comando pragma do namespace&\# 32; NamespacePath forem usados, o comando terá prioridade sobre a opção.
ms.assetid: d280f67a-a798-47c0-b8de-071c290dd216
ms.tgt_platform: multiple
title: namespace de pragma
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: b5f5e164632fef5a41e7233caf4fd154d1dafe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647696"
---
# <a name="pragma-namespace"></a>namespace de pragma

O comando de pré-processador do **namespace pragma** solicita que o compilador carregue o arquivo MOF no namespace especificado como *NamespacePath*. Se a opção de namespace do compilador MOF **-n** e o comando *NamespacePath* do **\# namespace pragma** forem usados, o comando terá prioridade sobre a opção.

O seguinte descreve a sintaxe:


```mof
#pragma namespace ("[Namespace]")
```



*\[ Namespace \]* é o namespace especificado.

Se você não especificar esse comando ou a opção de linha de comando equivalente, o compilador MOF usará o \\ namespace raiz padrão por padrão.

## <a name="remarks"></a>Comentários

Você pode exigir que os scripts e aplicativos de cliente usem uma conexão criptografada para autenticação adicionando o qualificador **RequiresEncryption** ao arquivo. MOF que cria o namespace. Você também pode modificar um namespace existente adicionando esse atributo e compilar o arquivo MOF novamente. Para obter mais informações sobre como usar o **RequiresEncryption**, consulte [exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como posicionar classes ou instâncias no namespace "raiz do \\ teste".


```mof
#pragma namespace ("\\\\.\\Root\\Test")
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[**Qualificadores WMI padrão**](standard-wmi-qualifiers.md)
</dt> <dt>

[Comandos de pré-processador](preprocessor-commands.md)
</dt> </dl>

 

 





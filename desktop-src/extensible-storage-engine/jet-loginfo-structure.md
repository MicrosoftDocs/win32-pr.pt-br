---
description: 'Saiba mais sobre: estrutura de JET_LOGINFO'
title: Estrutura de JET_LOGINFO
TOCTitle: JET_LOGINFO Structure
ms:assetid: b34b3f24-5d19-4e11-a657-a0e59204d628
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294063(v=EXCHG.10)
ms:contentKeyID: 32765678
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f5619211a5fc76bb080b81b22c08c9e369abf93
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983159"
---
# <a name="jet_loginfo-structure"></a>Estrutura de JET_LOGINFO


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_loginfo-structure"></a>Estrutura de JET_LOGINFO

A estrutura de **JET_LOGINFO** retorna informações estruturadas sobre o conjunto de arquivos de log de transações que devem ser parte de um conjunto de arquivos de backup. A estrutura de **JET_LOGINFO** é o conjunto mínimo de informações necessárias para representar um intervalo de logs que é recuperado com [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) ou especificado para uma recuperação complexa com [JetExternalRestore2](./jetexternalrestore2-function.md).

```cpp
typedef struct {
  unsigned long cbSize;
  unsigned long ulGenLow;
  unsigned long ulGenHigh;
  tchar szBaseName[JET_BASE_NAME_LENGTH + 1];
} JET_LOGINFO;
```

### <a name="members"></a>Membros

**cbSize**

O tamanho da estrutura, em bytes.

Esse membro permite a expansão futura dessa estrutura, ao mesmo tempo em que habilita a compatibilidade com versões anteriores. Ele deve sempre ser definido como sizeof (JET_LOGINFO).

**ulGenLow**

O número do arquivo de log mais baixo (ou mais antigo) que é restaurado. A fidelidade total de um longo não assinado deve ser preservada, mas nas versões atuais do mecanismo esse número é um número hexadecimal no intervalo de 0x00000 a 0xFFFFF. Isso pode ser alterado em versões futuras.

**ulGenHigh**

O número de arquivo de log mais alto (ou mais recente) que é restaurado. A fidelidade total de um longo não assinado deve ser preservada, mas nas versões atuais do mecanismo esse número é um número hexadecimal no intervalo de 0x00000 a 0xFFFFF. Isso pode ser alterado em versões futuras.

**szBaseName**

O prefixo usado para nomear os arquivos de log de transações.

O valor retornado nesse membro é sempre igual à configuração de [JET_paramBaseName](./transaction-log-parameters.md) para a instância que gerou essas informações.

### <a name="remarks"></a>Comentários

Os arquivos de log de transações são nomeados de acordo com o nome base da instância e o número de geração do arquivo de log. O nome é do formato BBBXXXXX. Façam. BBB corresponde ao nome de base para o arquivo de log e tem sempre três caracteres de comprimento. XXXXX corresponde ao número de geração do arquivo de log em zero hexadecimal preenchido e tem sempre cinco caracteres de comprimento. LOG é a extensão de arquivo que é sempre fornecida para os arquivos de log de transações pelo mecanismo.

O uso dessas informações estruturadas não é recomendado porque faz com que o aplicativo tenha conhecimento profundo desse esquema de nomenclatura para arquivos de log de transações. Se o esquema de nomenclatura mudar no futuro, tal aplicativo deixará de funcionar corretamente. É concebível que o formato de log seja alterado para incorporar 8 dígitos hexadecimais no futuro. Os aplicativos devem usar a lista explícita de nomes de arquivos retornados por [JetGetLogInfo](./jetgetloginfo-function.md) em vez disso.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_LOGINFO_W</strong> (Unicode) e <strong>JET_LOGINFO_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte Também

[JetExternalRestore2](./jetexternalrestore2-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
